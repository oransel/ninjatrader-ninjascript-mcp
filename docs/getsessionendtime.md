# GetSessionEndTime()

Source: https://developer.ninjatrader.com/docs/desktop/getsessionendtime

---

# GetSessionEndTime()


## [Definition](https://developer.ninjatrader.com/docs/desktop/getsessionendtime#definition)


Returns the daily bar session ending time stamp relative to the current bar index value.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This method is ONLY intended for bars built from daily data. If called on intraday data, **GetSessionEndTime()** will return the [**Bars.GetTime()**](https://developer.ninjatrader.com/docs/desktop/gettime) value.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/getsessionendtime#method-return-value)


A DateTime structure that represents the daily bars ending time stamp at the desired bar index; intraday bars will return the time stamp at the current bar index value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/getsessionendtime#syntax)


`Bars.GetSessionEndTime(int index)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/getsessionendtime#parameters)


| --- |
| **index** | An int representing an absolute bar index value |


## [Examples](https://developer.ninjatrader.com/docs/desktop/getsessionendtime#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
   base.OnRender(chartControl, chartScale);
   // loop through only the rendered bars on the chart
   for (int barIndex = ChartBars.FromIndex; barIndex <= ChartBars.ToIndex; barIndex++)
   {
     // get the time stamp at the selected bar index value
     DateTime timeValue = Bars.GetSessionEndTime(barIndex);
     Print("Bar #" + barIndex + " time stamp is " + timeValue);
   }
```
