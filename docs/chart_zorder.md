# ZOrder

Source: https://developer.ninjatrader.com/docs/desktop/chart_zorder

---

# ZOrder


## [Definition](https://developer.ninjatrader.com/docs/desktop/chart_zorder#definition)


A unique identifier representing the index in which chart objects are drawn on the chart's Z-axis (front to back ordering). Objects with a higher ZOrder are drawn first.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


The ZOrder index should NOT be set using this property. Please use the dedicated [SetZOrder()](https://developer.ninjatrader.com/docs/desktop/setzorder) method for this purpose.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/chart_zorder#property-value)


A int value representing the order that the object is drawn. Default value is categorized by the type of object drawn, which will then increment for each instance of the chart object that is drawn. Each type of object will have a different default starting value to keep these objects separate:


| Chart Bars | 1 |
| --- | --- |
| NinjaScript Objects | 10001 |
| Global Draw Objects | 20001 |
| Draw Objects | 30001 |


## [Syntax](https://developer.ninjatrader.com/docs/desktop/chart_zorder#syntax)


ZOrder


## [Examples](https://developer.ninjatrader.com/docs/desktop/chart_zorder#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
  // call the base.OnRender() to ensure standard Plots work as designed
  base.OnRender(chartControl, chartScale);

  // Print the currently assigned ZOrder index for this NinjaScript object
  Print("Current ZOrder level is: " + ZOrder);
}
```
