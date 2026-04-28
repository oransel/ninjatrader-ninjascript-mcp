# ClearOutputWindow()

Source: https://developer.ninjatrader.com/docs/desktop/clearoutputwindow

---

# ClearOutputWindow()


## [Definition](https://developer.ninjatrader.com/docs/desktop/clearoutputwindow#definition)


Clears all data from the NinjaTrader **Output Window**.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


The ClearOutputWindow() method only targets the Output tab most recently determined by set **PrintTo** property.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/clearoutputwindow#method-return-value)


This method does not return a value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/clearoutputwindow#syntax)


`ClearOutputWindow()`


## [Examples](https://developer.ninjatrader.com/docs/desktop/clearoutputwindow#examples)


```csharp
protected override void OnStateChange()
{
   if (State == State.SetDefaults)
   {
     Name = "Examples Indicator";
     Description = @"An indicator used to demonstrate various NinjaScript methods and properties";
   }
   else if (State == State.Configure)
   {
     AddDataSeries(BarsPeriodType.Minute, 5);
   }

   else if(State == State.DataLoaded)
   {
     //clear the output window as soon as the bars data is loaded
     ClearOutputWindow();
   }
}
```
