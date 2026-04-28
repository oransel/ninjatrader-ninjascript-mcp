# NTMessageBoxSimple.Show()

Source: https://developer.ninjatrader.com/docs/desktop/ntmessageboxsimple_show

---

# NTMessageBoxSimple.Show()


## [Definition](https://developer.ninjatrader.com/docs/desktop/ntmessageboxsimple_show#definition)


Creates a message box window.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


For more information on using MessageBox windows, please see **.NET MessageBox Class Documentation** [here](https://docs.microsoft.com/en-us/dotnet/api/system.windows.messagebox?view=netframework-4.8).


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/ntmessageboxsimple_show#method-return-value)


**MessageBoxResult**; an enum representing the button press used to close the MessageBox window.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/ntmessageboxsimple_show#syntax)


`NTMessageBoxSimple.Show(Window input, string messageTxt, string caption, MessageBoxButton buttonSet, MessageBoxImage icon)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/ntmessageboxsimple_show#parameters)


| --- |
| **parent** | A Window (DependencyObject) which represents the owning window |
| **messageTxt** | The message body of the MessageBox window |
| **caption** | The header of the MessageBox window |
| **buttonSet** | A MesageBoxButton enum determining the buttons used for the MessageBox window |
| **icon** | A MesageBoxImage enum determining the icon used for the MessageBox window |


## [Examples](https://developer.ninjatrader.com/docs/desktop/ntmessageboxsimple_show#examples)


```csharp
// Create a MessageBox window from a Chart
ChartControl.Dispatcher.InvokeAsync(new Action(() => {
   NinjaTrader.Gui.Tools.NTMessageBoxSimple.Show(Window.GetWindow(ChartControl.OwnerChart as DependencyObject), "Message Body", "Message Header", MessageBoxButton.OK, MessageBoxImage.None);
}));

// Create a MessageBox window from a button press in an AddOn**
private void OnMenuItemClick(object sender, RoutedEventArgs e)
{
    NinjaTrader.Gui.Tools.NTMessageBoxSimple.Show(Window.GetWindow(e.Source as DependencyObject), "Message Body", "Message Header", MessageBoxButton.OK, MessageBoxImage.None);
```
