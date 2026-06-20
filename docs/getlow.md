# GetLow()

Source: https://developer.ninjatrader.com/docs/desktop/getlow

---

# GetLow()


## [Definition](https://developer.ninjatrader.com/docs/desktop/getlow#definition)


Returns the low price at the selected bar index value.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/getlow#method-return-value)


A **double** value that represents the low price at the desired bar index.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/getlow#syntax)


`Bars.GetLow(int index)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/getlow#parameters)


| --- |
| **index** | An int representing an absolute bar index value |


## [Examples](https://developer.ninjatrader.com/docs/desktop/getlow#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
   base.OnRender(chartControl, chartScale);
   // loop through only the rendered bars on the chart
   for(int barIndex = ChartBars.FromIndex; barIndex <= ChartBars.ToIndex; barIndex++)
   {
     // get the low price at the selected bar index value
     double lowPrice = Bars.GetLow(barIndex);
     Print("Bar #" + barIndex + " low price is " + lowPrice);
   }
}
```
