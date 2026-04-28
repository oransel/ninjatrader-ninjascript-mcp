# IsYAxisDisplayedOverlay

Source: https://developer.ninjatrader.com/docs/desktop/isyaxisdisplayedoverlay_chartpanel

---

# IsYAxisDisplayedOverlay


## [Definition](https://developer.ninjatrader.com/docs/desktop/isyaxisdisplayedoverlay_chartpanel#definition)


Indicates any objects configured in the panel are using the Overlay scale justification.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/isyaxisdisplayedoverlay_chartpanel#property-value)


A bool indicating any objects use the Overlay scale justification.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/isyaxisdisplayedoverlay_chartpanel#syntax)


`ChartPanel.IsYAxisDisplayedOverlay`


## [Examples](https://developer.ninjatrader.com/docs/desktop/isyaxisdisplayedoverlay_chartpanel#examples)
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Based on the image below, **IsYAxisDisplayedOverlay** is set to True, since the SMA indicator is using the Overlay scale justification.


![ChartPanel_IsYAxisDisplayedOverlay](https://cdn.sanity.io/images/1hlwceal/production/302676489d95ab8ef47c292f209c9a8ae7bfcee9-716x533.png)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
    base.OnRender(chartControl, chartScale);

    // Trigger an alert when the Overlay scale justification is used
    if (ChartPanel.IsYAxisDisplayedOverlay)
        Alert("overlayAlert", Priority.Low, "It is not recommended to use 'Overlay' with this indicator", "", 300, Brushes.Yellow, Brushes.Black);
}
```
