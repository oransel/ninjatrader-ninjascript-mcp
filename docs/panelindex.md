# PanelIndex

Source: https://developer.ninjatrader.com/docs/desktop/panelindex

---

# PanelIndex


## [Definition](https://developer.ninjatrader.com/docs/desktop/panelindex#definition)


The panel on which the chart scale resides.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This value is NOT the same value as the indicator's **PanelUI**. **PanelIndex** will provide the actual indexed value of the chart panel used for this chart scale.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/panelindex#property-value)


An **int** value representing the panel as an index value which starts at 0 and will increment for each panel configured on the chart. This property is read-only.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/panelindex#syntax)


`<chartscale>.PanelIndex`


## [Examples](https://developer.ninjatrader.com/docs/desktop/panelindex#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
   // the index value of the panel (not the same as the panelUI)
   int     panel     = chartScale.PanelIndex;
   Print("panel: " + panel);
}
```
