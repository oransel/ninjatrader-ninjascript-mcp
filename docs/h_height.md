# H (Height)

Source: https://developer.ninjatrader.com/docs/desktop/h_height

---

# H (Height)


## [Definition](https://developer.ninjatrader.com/docs/desktop/h_height#definition)


Indicates the height (in pixels) of the rendered area of the chart panel.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


The paintable area does not extend all the way to the top edge of the panel itself, as seen in the image below.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/h_height#property-value)


A int representing the height of the panel in pixels.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/h_height#syntax)


`ChartPanel.H`


## [Examples](https://developer.ninjatrader.com/docs/desktop/h_height#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
    base.OnRender(chartControl, chartScale);

    // Print the height of the panel
    Print(ChartPanel.H);
}
```


Based on the image below, H reveals that the paintable area of the chart panel is 69 pixels high.


![ChartPanel_H](https://cdn.sanity.io/images/1hlwceal/production/7276ede93b5a4b991340373863b85b320cbea7f4-534x433.png)
