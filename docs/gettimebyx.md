# GetTimeByX()

Source: https://developer.ninjatrader.com/docs/desktop/gettimebyx

---

# GetTimeByX()


## [Definition](https://developer.ninjatrader.com/docs/desktop/gettimebyx#definition)


Returns a time value related to the primary **Bars** slot index at a specified x-coordinate relative to the **ChartControl**.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Since the time is based upon a coordinate of the chart canvas, the value returned by **GetTimeByX()** can be expected to change as new bars are painted on the chart, or as the chart is scrolled backward or forward on the x-axis.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/gettimebyx#method-return-value)


A **DateTime** object corresponding to a slot index at a specified x-coordinate.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/gettimebyx#syntax)


`<chartcontrol>.GetTimeByX(int x)`


## [Method Parameters](https://developer.ninjatrader.com/docs/desktop/gettimebyx#method-parameters)


| --- |
| x | The x-coordinate used to find a time value |


## [Examples](https://developer.ninjatrader.com/docs/desktop/gettimebyx#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
   // Find the timestamp of the bar at x-coordinate 100
   DateTime slotTime = chartControl.GetTimeByX(100);
 
   // Print the date of slotTime
   Print(slotTime);
}
```
