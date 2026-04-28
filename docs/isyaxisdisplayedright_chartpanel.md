# IsYAxisDisplayedRight

Source: https://developer.ninjatrader.com/docs/desktop/isyaxisdisplayedright_chartpanel

---

# IsYAxisDisplayedRight


## [Definition](https://developer.ninjatrader.com/docs/desktop/isyaxisdisplayedright_chartpanel#definition)


Indicates the y-axis is visible on the right side of the chart panel.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/isyaxisdisplayedright_chartpanel#property-value)


A **bool** indicating the y-axis is visible to the right


## [Syntax](https://developer.ninjatrader.com/docs/desktop/isyaxisdisplayedright_chartpanel#syntax)


`ChartPanel.IsYAxisDisplayedRight`


## [Examples](https://developer.ninjatrader.com/docs/desktop/isyaxisdisplayedright_chartpanel#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)

{

   base.OnRender(chartControl, chartScale);

   // Print a message if the y-axis is visible on the right

   if (ChartPanel.IsYAxisDisplayedRight)

       Print("The y-axis is visible on the right");

}
```


Based on the image below, **IsYAxisDisplayedRight** confirms that the y-axis is not displayed on the right. The property would be set to false when applied in either chart panel in this instance.


![ChartPanel_IsYAxisDisplayedRight](https://cdn.sanity.io/images/1hlwceal/production/20d23d58fe540df5aeaf13c0934c42f93b186e86-534x433.png)
