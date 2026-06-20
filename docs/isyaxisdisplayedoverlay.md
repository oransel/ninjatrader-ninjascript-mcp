# IsYAxisDisplayedOverlay

Source: https://developer.ninjatrader.com/docs/desktop/isyaxisdisplayedoverlay

---

# IsYAxisDisplayedOverlay


## [Definition](https://developer.ninjatrader.com/docs/desktop/isyaxisdisplayedoverlay#definition)


Indicates an object on the chart is using the Overlay scale justification.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/isyaxisdisplayedoverlay#property-value)


A boolean value. When **True**, indicates that one or more objects on the chart are using the Overlay scale justification; otherwise **False**.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/isyaxisdisplayedoverlay#syntax)


`<chartcontrol>.IsYAxisDisplayedOverlay`


## [Examples](https://developer.ninjatrader.com/docs/desktop/isyaxisdisplayedoverlay#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
   // Print the value of IsYAxisDisplayedOverlay
   Print("Is Overlay used? " + chartControl.IsYAxisDisplayedOverlay);
}
```


Based on the image below, **IsYAxisDisplayedOverlay** confirms that an object on the chart, in this case an SMA indicator, is using the Overlay scale justification.


![ChartControl_IsXAxisDisplayedOverlay](https://cdn.sanity.io/images/1hlwceal/production/8681385f146613b3a73a4831e1808f14fc5d4b49-732x541.png)
