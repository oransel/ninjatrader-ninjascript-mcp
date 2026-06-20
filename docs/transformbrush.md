# TransformBrush()

Source: https://developer.ninjatrader.com/docs/desktop/transformbrush

---

# TransformBrush()


## [Definition](https://developer.ninjatrader.com/docs/desktop/transformbrush#definition)


Scales a non-solid color brush used for rendering the chart style to properly display in NinjaTrader.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This method has no impact on solid color brushes.  You would only need to pass in either a linear or radial gradient brush.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/transformbrush#method-return-value)


This method does not return a value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/transformbrush#syntax)


`TransformBrush(SharpDX.Direct2D1.Brush brush, RectangleF rect)`


## [Method Parameters](https://developer.ninjatrader.com/docs/desktop/transformbrush#method-parameters)


| Parameter | Description |
| --- | --- |
| brush | A [SharpDX.Direct2D1.Brush](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_brush) object representing the brush used to render |
| rect | A [RectangleF](https://msdn.microsoft.com/en-us/library/system.drawing.rectanglef%28v=vs.110%29.aspx) structure representing the rectangle to be rendered |


## [Examples](https://developer.ninjatrader.com/docs/desktop/transformbrush#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale, ChartBars chartBars)
{
		TransformBrush(brush, rect);
}
```
