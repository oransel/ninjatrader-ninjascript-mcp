# W (Width)

Source: https://developer.ninjatrader.com/docs/desktop/w_width_chartpanel

---

# W (Width)


## [Definition](https://developer.ninjatrader.com/docs/desktop/w_width_chartpanel#definition)


Indicates the width (in pixels) of the paintable area of the chart panel.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


The paintable area does not extend all the way to the right edge of the panel itself, as seen in the image below.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/w_width_chartpanel#property-value)


A **int** representing the width of the panel in pixels


## [Syntax](https://developer.ninjatrader.com/docs/desktop/w_width_chartpanel#syntax)


`ChartPanel.W`


## [Example](https://developer.ninjatrader.com/docs/desktop/w_width_chartpanel#example)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
  base.OnRender(chartControl, chartScale);

  // Print the width of the panel
  Print(ChartPanel.W);
}
```


Based on the image below, W reveals that the chart panel is 451 pixels wide.


![chartpanel_w](https://cdn.sanity.io/images/1hlwceal/production/272505438485c2b076f0066d6626100aea434e0b-534x433.png)
