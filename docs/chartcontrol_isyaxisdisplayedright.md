# IsYAxisDisplayedRight

Source: https://developer.ninjatrader.com/docs/desktop/chartcontrol_isyaxisdisplayedright

---

# IsYAxisDisplayedRight


## [Definition](https://developer.ninjatrader.com/docs/desktop/chartcontrol_isyaxisdisplayedright#definition)


Indicates the y-axis displays (in any chart panel) to the right side of the chart.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/chartcontrol_isyaxisdisplayedright#property-value)


A boolean value. When **True**, indicates that the y-axis displays to the right of the chart canvas; otherwise **False**.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/chartcontrol_isyaxisdisplayedright#syntax)


`<chartcontrol>.IsYAxisDisplayedRight`


## [Examples](https://developer.ninjatrader.com/docs/desktop/chartcontrol_isyaxisdisplayedright#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
   // Print the value of IsYAxisDisplayedRight
   Print("Y-Axis visible to the right of the chart canvas? " + chartControl.IsYAxisDisplayedRight);
}
```


Based on the image below, **IsYAxisDisplayedRight** confirms that the y-axis is not displayed to the right of the chart canvas.


![ChartControl_IsYAxisDisplayedRight](https://cdn.sanity.io/images/1hlwceal/production/dcbfbe76e74b6dae7aca3c477875e914d04a5dfa-575x429.png)
