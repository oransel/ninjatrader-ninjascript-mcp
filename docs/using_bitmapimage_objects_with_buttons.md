# Using BitmapImage objects with Buttons

Source: https://developer.ninjatrader.com/docs/desktop/using_bitmapimage_objects_with_buttons

---

# Using BitmapImage objects with Buttons


## [Images as Buttons Overview](https://developer.ninjatrader.com/docs/desktop/using_bitmapimage_objects_with_buttons#images-as-buttons-overview)


BitmapImage objects can be used to apply an image as a background to a Button object added to a NinjaTrader window.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


The following topic covers methods and properties outside of the NinjaScript libraries. Most of the items covered in the example below belong to .NET's System.Windows.Media.Imaging and System.Windows.Controls namespaces. More information on these namespaces can be found at the links below:


- [System.Windows.Controls](https://learn.microsoft.com/en-us/dotnet/api/system.windows.controls?view=windowsdesktop-7.0)
- [System.Windows.Media.Imaging](https://learn.microsoft.com/en-us/dotnet/api/system.windows.media.imaging?view=windowsdesktop-7.0)


Using an image as the background for a button can be achieved through a fairly straightforward process using some of the .NET framework's Controls and Imaging methods


There are a few best practices to keep in mind when working with Buttons:


- Dispose of any leftover objects in State.Terminated for efficient memory use
- Use your object's main Dispatcher when adding or removing Buttons to or from your chart, to ensure that the correct thread is used
- Be aware of the proper States in which to initialize objects related to the Button (State.Configure), apply the Button (State.Historical), and dispose of unneeded objects (State.Terminated)


## [Adding a Button to a Chart Toolbar Using an Image as the Background](https://developer.ninjatrader.com/docs/desktop/using_bitmapimage_objects_with_buttons#adding-a-button-to-a-chart-toolbar-using-an-image-as-the-background)


The example below walks through the process of adding a Button to a chart toolbar specifically, and applying a .jpg image as the Button's background. This example also displays several best practices when working with Buttons, such as proper object disposal and ensuring that the Button is not populated when the indicator is applied in an inactive chart tab.


```csharp
//Add the following Using statements
using System.Windows.Media.Imaging;
using System.Windows.Controls;

public class addButton : Indicator
{
  // Define a Chart object to refer to the chart on which the indicator resides
  private Chart chartWindow;

  // Define a Button
  private System.Windows.Controls.Button myButton = null;

  // Instantiate a BitmapImage to hold an image
  BitmapImage myBitmapImage = new BitmapImage();

  // Instantiate an ImageBrush to apply to the Button
  ImageBrush backgroundImage = new ImageBrush();

  private bool IsToolBarButtonAdded;

  protected override void OnStateChange()
  {
      if (State == State.Configure)
      {
          // Assign an image on the filesystem to the BitmapImage.

           // This example assumes that a jpg image named "ButtonBackground" resides in the install directory
          myBitmapImage.BeginInit();
          myBitmapImage.UriSource = new Uri(NinjaTrader.Core.Globals.InstallDir + "ButtonBackground.jpg");
          myBitmapImage.EndInit();

          // Assign the BitmapImage as the ImageSource of the ImageBrush
          backgroundImage.ImageSource = myBitmapImage;
      }
      else if (State == State.Historical)
      {
          //Call the custom addButtonToToolbar method in State.Historical to ensure it is only done when applied to a chart

           // -- not when loaded in the Indicators window
          if (!IsToolBarButtonAdded) AddButtonToToolbar();
      }
      else if (State == State.Terminated)
      {
          //Call a custom method to dispose of any leftover objects in State.Terminated
          DisposeCleanUp();
      }
  }

  private void AddButtonToToolbar()
  {
      // Use this.Dispatcher to ensure code is executed on the proper thread
      ChartControl.Dispatcher.InvokeAsync((Action)(() =>
      {

          //Obtain the Chart on which the indicator is configured
          chartWindow = Window.GetWindow(this.ChartControl.Parent) as Chart;
          if (chartWindow == null)
          {
              Print("chartWindow == null");
              return;
          }

          // Create a style to apply to the button
          Style s = new Style();
          s.TargetType = typeof(System.Windows.Controls.Button);
          s.Setters.Add(new Setter(System.Windows.Controls.Button.FontSizeProperty, 11.0));
          s.Setters.Add(new Setter(System.Windows.Controls.Button.BackgroundProperty, Brushes.Orange));
          s.Setters.Add(new Setter(System.Windows.Controls.Button.ForegroundProperty, Brushes.Black));
          s.Setters.Add(new Setter(System.Windows.Controls.Button.FontFamilyProperty, new FontFamily("Arial")));
          s.Setters.Add(new Setter(System.Windows.Controls.Button.FontWeightProperty, FontWeights.Bold));

          // Instantiate the Button
          myButton = new System.Windows.Controls.Button();

          //Set Button Style
          myButton.Style = s;

          // Set the Imagebrush as the Background for the Button
          myButton.Background = backgroundImage;

          myButton.Content = "Click Here";
          myButton.IsEnabled = true;
          myButton.HorizontalAlignment = HorizontalAlignment.Left;

          // Add the Button to the Chart's Toolbar
          chartWindow.MainMenu.Add(myButton);

          //Prevent the Button From Displaying when WorkSpace Opens if it is not in an active tab
          myButton.Visibility = Visibility.Collapsed;
          foreach (TabItem tab in this.chartWindow.MainTabControl.Items)
          {
              if ((tab.Content as ChartTab).ChartControl == this.ChartControl

                   && tab == this.chartWindow.MainTabControl.SelectedItem)
              {
                  myButton.Visibility = Visibility.Visible;
              }
          }
          IsToolBarButtonAdded = true;
      }));
  }

  private void DisposeCleanUp()
  {
      //ChartWindow Null Check
      if (chartWindow != null)
      {
          //Dispatcher used to Assure Executed on UI Thread
          ChartControl.Dispatcher.InvokeAsync((Action)(() =>
          {
              //Button Null Check
              if (myButton != null)
              {
                  //Remove Button from Indicator's Chart ToolBar
                  chartWindow.MainMenu.Remove(myButton);
              }
          }));
      }
  }
}
```
