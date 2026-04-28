# Line Class

Source: https://developer.ninjatrader.com/docs/desktop/line_class

---

# Line Class


## [Definition](https://developer.ninjatrader.com/docs/desktop/line_class#definition)


Objects derived from the **Line** class are used to characterize how an oscillator line is visually displayed (plotted) on a chart.


## [Properties](https://developer.ninjatrader.com/docs/desktop/line_class#properties)


| --- |
| Brush | The System.Windows.Media.Brush used to construct the line ([reference](https://msdn.microsoft.com/en-us/library/system.windows.media.brushes%28v=vs.110%29.aspx)) |
| BrushDX | A [SharpDX.Direct2D1.Brush](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_brush) used to actually render the line. |
| DashStyleDX | A [SharpDX.Direct2D1.DashStyle](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_strokestyle_dashstyle) used to render the stroke style.


**Note**: To avoid and resolve access violation exceptions, please see Warning and examples remarked below |
| DashStyleHelper | A dashstyle used to construct the stroke. Possible values are:

- **DashStyleHelper.Dash**
- **DashStyleHelper.DashDot**
- **DashStyleHelper.DashDotDot**
- **DashStyleHelper.Dot**
- **DashStyleHelper.Solid** |
| Name | A **string** representing the name of the line |
| RenderTarget | The [RenderTarget](https://developer.ninjatrader.com/docs/desktop/rendertarget) drawing context used for the line. |
| StrokeStyle | A [SharpDX.Direct2D1.StrokeStyle](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_strokestyle) |
| Value | A **double** representing the value of the line |
| Width | A **float** representing the width in pixels |


## [Examples](https://developer.ninjatrader.com/docs/desktop/line_class#examples)


See the [AddLine()](https://developer.ninjatrader.com/docs/desktop/addline) method for examples.
