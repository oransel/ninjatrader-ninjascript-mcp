# TimePainted

Source: https://developer.ninjatrader.com/docs/desktop/timepainted

---

# TimePainted


## [Definition](https://developer.ninjatrader.com/docs/desktop/timepainted#definition)


Indicates the range of time in which bars are painted on the visible chart canvas.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/timepainted#property-value)


A TimeSpan measuring the difference between the earliest and latest times at which bars are painted on the chart.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/timepainted#syntax)


``<chartcontrol>.TimePainted`


## [Examples](https://developer.ninjatrader.com/docs/desktop/timepainted#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
   // Print a message if less than three hours' worth of data is painted on the chart canvas
   if(chartControl.TimePainted.Hours < 3)
       Print(String.Format("It is recommended to view at least three hours worth of data on your chart with this indicator. You are currently viewing {0}", chartControl.TimePainted));
}
```

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


TimePainted is intended to be used when Non-Equidistant (time-based) bar spacing is enabled on the chart. Otherwise, it will have a value of 0.
