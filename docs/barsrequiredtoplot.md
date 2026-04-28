# BarsRequiredToPlot

Source: https://developer.ninjatrader.com/docs/desktop/barsrequiredtoplot

---

# BarsRequiredToPlot


## [Definition](https://developer.ninjatrader.com/docs/desktop/barsrequiredtoplot#definition)


The number of bars on a chart required before the script plots. By default, the value is 20 bars.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This property is NOT the same as a minimum number of bars required to calculate the script values. OnBarUpdate will always start calculating for the first bar on the chart (CurrentBar 0)


## [Property Value](https://developer.ninjatrader.com/docs/desktop/barsrequiredtoplot#property-value)


An **int** value that represents the minimum number of bars required.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/barsrequiredtoplot#syntax)


`BarsRequiredToPlot`


## [Examples](https://developer.ninjatrader.com/docs/desktop/barsrequiredtoplot#examples)


```csharp
protected override void OnStateChange()
{
     if (State == State.SetDefaults)
     {
          BarsRequiredToPlot = 10; // Do not plot until the 11th bar on the chart
          AddPlot(Brushes.Orange, "SMA");
     }
}
```
