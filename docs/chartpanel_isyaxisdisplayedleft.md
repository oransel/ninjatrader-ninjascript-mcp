# IsYAxisDisplayedLeft

Source: https://developer.ninjatrader.com/docs/desktop/chartpanel_isyaxisdisplayedleft

---

# IsYAxisDisplayedLeft


## [Definition](https://developer.ninjatrader.com/docs/desktop/chartpanel_isyaxisdisplayedleft#definition)


Indicates the y-axis is visible on the left side of the chart panel.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/chartpanel_isyaxisdisplayedleft#property-value)


A bool indicating the y-axis is visible to the left


## [Syntax](https://developer.ninjatrader.com/docs/desktop/chartpanel_isyaxisdisplayedleft#syntax)


`ChartPanel.IsYAxisDisplayedLeft`


## [Examples](https://developer.ninjatrader.com/docs/desktop/chartpanel_isyaxisdisplayedleft#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
   base.OnRender(chartControl, chartScale);

   // Print a message if the y-axis is visible on the left
   if (ChartPanel.IsYAxisDisplayedLeft)
       Print("The y-axis is visible on the left");
}
```


Based on the image below, **IsYAxisDisplayedLeft** confirms that the y-axis displays to the left. In this image, the property would be set to true when applied to either chart panel.


![ChartPanel_IsYAxisDisplayedLeft](https://cdn.sanity.io/images/1hlwceal/production/b6f7a9d5e000f73c1475c0972aaf49a2bcf74c13-534x433.png)
