# OnDataPoint()

Source: https://developer.ninjatrader.com/docs/desktop/ondatapoint

---

# OnDataPoint()


## [Definition](https://developer.ninjatrader.com/docs/desktop/ondatapoint#definition)


Called for each record in the corresponding base dataset used to build the BarType (i.e., for every tick, minute, or day). The **OnDataPoint()** method is where you should adjust data points (bar values) of your series through [**AddBar()**](https://developer.ninjatrader.com/docs/desktop/addbar) and [**UpdateBar()**](https://developer.ninjatrader.com/docs/desktop/updatebar). See also the [**BuiltFrom**](https://developer.ninjatrader.com/docs/desktop/builtfrom) property.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


- Historical data processing receives a single update for every base bar determined by the **BuiltFrom** property.
- When using [**TickReplay**](https://ninjatrader.com/support/helpGuides/nt8/?tick_replay.htm), historical updates will call for every tick handled by the core regardless of the **BuiltFrom** property defined.
- Once transitioned to real-time, updates will call on every tick processed by the core.
- The bid/ask parameters will ONLY be available historically when using [**Tick Replay**](https://ninjatrader.com/support/helpGuides/nt8/?tick_replay.htm), unless you are using a 1-tick series.
- **isBar** could be true in case the BarsSeries was internally copied to another BarsSeries and is only needed for [**IsTimeBased**](https://developer.ninjatrader.com/docs/desktop/istimebased) = true BarsTypes (e.g. Second/Minute/Day...).


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/ondatapoint#method-return-value)


This method does not return a value.


## [Method Parameters](https://developer.ninjatrader.com/docs/desktop/ondatapoint#method-parameters)


| --- |
| bars | The Bars object of your bars type |
| open | A **double** value representing the open price |
| high | A **double** value representing the high price |
| low | A **double** value representing the low price |
| close | A **double** value representing the close price |
| time | A DateTime value representing the time |
| volume | A long value representing the volume |
| isBar | A bool value representing if **OnDataPoint** should treat the timestamp as an already built bar instead of an intrabar timestamp. |
| bid | A **double** value representing the bid price |
| ask | A **double** value representing the ask price |


## [Syntax](https://developer.ninjatrader.com/docs/desktop/ondatapoint#syntax)


You must override the method in your Bars Type with the following syntax.


`protected override void OnDataPoint(Bars bars, double open, double high, double low, double close, DateTime time, long volume, bool isBar, double bid, double ask) { }`


## [Examples](https://developer.ninjatrader.com/docs/desktop/ondatapoint#examples)


```csharp
protected override void OnDataPoint(Bars bars, double open, double high, double low, double close, DateTime time, long volume, bool isBar, double bid, double ask)
{
     int minIndex;

     // Create the first data point of our series
     if (bars.Count == 0)
     {
         minIndex = 0;
         AddBar(bars, open, high, low, close, TimeToBarTime(time, (int) bars.BarsPeriod.Value), volume);
     }
     // Update our data point with the latest information
     else if ((time.Month <= bars.LastBarTime.Month && time.Year == bars.LastBarTime.Year) || time.Year < bars.LastBarTime.Year)
     {
         if (high != bars.GetHigh(bars.Count - 1) || low != bars.GetLow(bars.Count - 1) ||
               close != bars.GetClose(bars.Count - 1) || volume > 0)
         {
               minIndex = bars.Count - 1;
               UpdateBar(bars, high, low, close, bars.LastBarTime, volume);
         }
         else
               minIndex = -1;
     }
     // Add new data points
     else
     {
         minIndex = bars.Count;
         AddBar(bars, open, high, low, close, time, (long)Math.Min(volumeTmp, bars.BarsPeriod.Value));
     }
     FirstBarAmended = minIndex;
}
```
