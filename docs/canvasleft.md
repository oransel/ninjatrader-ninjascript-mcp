# CanvasLeft

Source: https://developer.ninjatrader.com/docs/desktop/canvasleft

---

# CanvasLeft


## [Definition](https://developer.ninjatrader.com/docs/desktop/canvasleft#definition)


Indicates the x-coordinate (in pixels) of the beginning of the chart canvas area.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/canvasleft#property-value)


A **double** representing the beginning of the chart canvas area.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/canvasleft#syntax)


`<chartcontrol>.CanvasLeft`


## [Examples](https://developer.ninjatrader.com/docs/desktop/canvasleft#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
    // Store the beginning and ending x-coordinates of the canvas area
    double canvasBeginCoordinate = chartControl.CanvasLeft;
    double canvasEndCoordinate = chartControl.CanvasRight;
    // Print the stored values
    Print(String.Format("Chart canvas begins at x-coordinate {0} and ends at x-coordinate {1}", canvasBeginCoordinate, canvasEndCoordinate));
}
```


Based on the image below, CanvasLeft reveals that the chart canvas area begins at x-coordinate 53.


![ChartControl_CanvasLeft](https://cdn.sanity.io/images/1hlwceal/production/15a88a12f954be17f806e77636bf43698cf46e3f-575x550.png)
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


When no data series are left-aligned on a chart, CanvasLeft will return 0, representing the x-coordinate origin, because the chart canvas will begin at coordinate 0.
