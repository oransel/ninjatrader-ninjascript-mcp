# GetHigh()

Source: https://developer.ninjatrader.com/docs/desktop/gethigh

---

# GetHigh()


## [Definition](https://developer.ninjatrader.com/docs/desktop/gethigh#definition)


Returns the high price at the selected bar index value.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/gethigh#method-return-value)


A **double** value that represents the high price at the desired bar index.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/gethigh#syntax)


`Bars.GetHigh(int index)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/gethigh#parameters)


| --- |
| **index** | An int representing an absolute bar index value |


## [Examples](https://developer.ninjatrader.com/docs/desktop/gethigh#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
   base.OnRender(chartControl, chartScale);
   // loop through only the rendered bars on the chart
   for(int barIndex = ChartBars.FromIndex; barIndex <= ChartBars.ToIndex; barIndex++)
   {
     // get the high price at the selected bar index value
     double highPrice = Bars.GetHigh(barIndex);
     Print("Bar #" + barIndex + " high price is " + highPrice);
   }
}
```
