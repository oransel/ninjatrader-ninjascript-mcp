# IsFirstBarOfSessionByIndex()

Source: https://developer.ninjatrader.com/docs/desktop/isfirstbarofsessionbyindex

---

# IsFirstBarOfSessionByIndex()


## [Definition](https://developer.ninjatrader.com/docs/desktop/isfirstbarofsessionbyindex#definition)


Indicates if the selected bar index value is the first bar of a trading session.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/isfirstbarofsessionbyindex#property-value)


This property returns true if the bar is the first bar of a session; otherwise, false. This property is read-only.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/isfirstbarofsessionbyindex#syntax)


`Bars.IsFirstBarOfSessionByIndex(int index)`


## [Warning](https://developer.ninjatrader.com/docs/desktop/isfirstbarofsessionbyindex#warning)
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


This property will always return false on non-intraday bar periods (e.g., Day, Month, etc).


## [Parameters](https://developer.ninjatrader.com/docs/desktop/isfirstbarofsessionbyindex#parameters)


| --- |
| **index** | An int representing an absolute bar index value |


## [Examples](https://developer.ninjatrader.com/docs/desktop/isfirstbarofsessionbyindex#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
    base.OnRender(chartControl, chartScale);
    // loop through only the rendered bars on the chart
    for(int barIndex = ChartBars.FromIndex; barIndex <= ChartBars.ToIndex; barIndex++)
    {
        // check if the rendered bar is the first bar of the trading session
        if (Bars.IsFirstBarOfSessionByIndex(barIndex))
        {
            DateTime slotTimeAtBarIndex = chartControl.GetTimeBySlotIndex(barIndex);
            Print(string.Format("Bar index {0} was the first bar of the session at slot time {1}.", barIndex, slotTimeAtBarIndex));
        }
    }
}
```
