# BarsArray

Source: https://developer.ninjatrader.com/docs/desktop/chartcontrol_barsarray

---

# BarsArray


## [Definition](https://developer.ninjatrader.com/docs/desktop/chartcontrol_barsarray#definition)


Provides a collection of **ChartBars** objects currently configured on the chart.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/chartcontrol_barsarray#property-value)


An **ObservableCollection** of **ChartBars** objects.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/chartcontrol_barsarray#syntax)


`<chartcontrol>.BarsArray`


## [Examples](https://developer.ninjatrader.com/docs/desktop/chartcontrol_barsarray#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
   // Instantiate a new <chartcontrol`>.BarsArray collection
   System.Collections.ObjectModel.ObservableCollection<chartbars> myChartBars = chartControl.BarsArray;
 
   // Print the number of bars in each Bars object within the <chartcontrol`>.BarsArray collection
   foreach(ChartBars bars in myChartBars)
   {
       Print(bars.Bars.Count);
   }
}
```
