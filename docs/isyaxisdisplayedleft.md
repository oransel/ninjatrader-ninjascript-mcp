# IsYAxisDisplayedLeft

Source: https://developer.ninjatrader.com/docs/desktop/isyaxisdisplayedleft

---

# IsYAxisDisplayedLeft


## [Definition](https://developer.ninjatrader.com/docs/desktop/isyaxisdisplayedleft#definition)


Indicates the y-axis displays (in any chart panel) to the left side of the chart.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/isyaxisdisplayedleft#property-value)


A **boolean** value. When True, indicates that the y-axis displays to the left of the chart canvas; otherwise False.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/isyaxisdisplayedleft#syntax)


`<ChartControl>.IsYAxisDisplayedLeft`


## [Examples](https://developer.ninjatrader.com/docs/desktop/isyaxisdisplayedleft#examples)


protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
  // Print the value of IsYAxisDisplayedLeft
  Print("Y-Axis visible to the left of the chart canvas? " + chartControl.IsYAxisDisplayedLeft);
}


Based on the image below, IsYAxisDisplayedLeft confirms that the y-axis displays to the left of the chart canvas.


![ChartControl_isYAxisDisplayedLeft](https://cdn.sanity.io/images/1hlwceal/production/1a8a2e6f6f5dd77dcd5c74433f52018c36346c4e-575x429.png)
