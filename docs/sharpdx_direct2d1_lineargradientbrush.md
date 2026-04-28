# SharpDX.Direct2D1.LinearGradientBrush

Source: https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_lineargradientbrush

---

# SharpDX.Direct2D1.LinearGradientBrush
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


Disclaimer: The **SharpDX SDK Reference** section was compiled from the official **SharpDX Documentation** and was NOT authored by NinjaTrader. The contents of this section are provided as-is and only cover a fraction of what is available from the SharpDX SDK. This page was intended only as a reference guide to help you get started with some of the 2D Graphics concepts used in the NinjaTrader.Custom assembly. Please refer to the official SharpDX Documentation for additional members not covered in this reference. For more seasoned graphic developers, the original MSDN **Direct2D1** and **DirectWrite** unmanaged API documentation can also be helpful for understanding the DirectX/Direct2D run-time environment. For NinjaScript development purposes, we document only essential members in the structure of this page.


## [Definition](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_lineargradientbrush#definition)


Paints an area with a linear gradient.


(See also [unmanaged API documentation](http://msdn.microsoft.com/en-us/library/dd371488.aspx))
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Notes:


- A **LinearGradientBrush** paints an area with a linear gradient along a line between the brush start point and end point. The gradient, defined by the brush [GradientStopCollection](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_lineargradientbrush_gradientstopcollection), is extruded perpendicular to this line, and then transformed by a brush [transform](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_brush_transform) (if specified).
- The start point and end point are described in the brush space and are mapped to the render target when the brush is used. Note the starting and ending coordinates are absolute, not relative to the render target size. A value of (0, 0) maps to the upper-left corner of the render target, while a value of (1, 1) maps one pixel diagonally away from (0, 0). If there is a nonidentity [brush transform](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_brush_transform) or [render target transform](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_rendertarget_transform), the brush [start point](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_lineargradientbrush_startpoint) and [end point](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_lineargradientbrush_endpoint) are also transformed.
- It is possible to specify a gradient axis that does not completely fill the area that is being painted. When this occurs, the ExtendMode, specified by the [GradientStopCollection](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_lineargradientbrush_gradientstopcollection), determines how the remaining area is painted.
- The **LinearGradientBrush** can only be used with the [render target](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_rendertarget) that created it or with the compatible targets for that render target.
- A **LinearGradientBrush** is a device-dependent resource: your application should create linear gradient brushes after it initializes the render target with which the brushes will be used, and recreate the brushes whenever the render target needs recreated. Please see the [MSDN Direct2D Resources Overview](https://msdn.microsoft.com/en-us/library/dd756757(v=vs.85).aspx) for more information.
- For convenience, Direct2D provides the [RadialGradientBrushProperties](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_lineargradientbrushproperties) function for creating a new **LinearGradientBrush**.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_lineargradientbrush#syntax)


`class SolidColorBrush`
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Tips:


- For NinjaScript Development purposes, you can use the [NinjaTrader.Gui.DxExtensions.ToDxBrush()](https://developer.ninjatrader.com/docs/desktop/todxbrush) helper method to convert a **System.Windows.Media.LinearGradientBrush** to a **SharpDX.Direct2D1.LinearGradientBrush**.
- General information on Direct2D brushes can be found on the [MSDN Direct2D Brushes Overview](https://msdn.microsoft.com/en-us/library/dd756651(v=vs.85).aspx).


## [Constructors](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_lineargradientbrush#constructors)


| Constructor | Description |
| --- | --- |
| new **LinearGradientBrush**([RenderTarget](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_rendertarget) renderTarget, [LinearGradientBrushProperties](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_lineargradientbrushproperties) linearGradientBrushProperties, [GradientStopCollection](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_gradientstopcollection) gradientStopCollection) | Creates a **LinearGradientBrush** that contains the specified gradient stops and has the specified transform and base opacity. |
| new **LinearGradientBrush**([RenderTarget](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_rendertarget) renderTarget, [LinearGradientBrushProperties](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_lineargradientbrushproperties) linearGradientBrushProperties, Nullable<[BrushProperties](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_brushproperties)> brushProperties, [GradientStopCollection](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_gradientstopcollection) gradientStopCollection) | Creates a **LinearGradientBrush** that contains the specified gradient stops and has the specified transform and base opacity. |


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_lineargradientbrush#methods-and-properties)


| Method/Property | Description |
| --- | --- |
| [Dispose()](https://developer.ninjatrader.com/docs/desktop/sharpdx_disposebase_dispose) | Performs application-defined tasks associated with freeing, releasing, or resetting unmanaged resources. (Inherited from [SharpDX.DisposeBase](https://developer.ninjatrader.com/docs/desktop/sharpdx_disposebase)). |
| [EndPoint](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_lineargradientbrush_endpoint) | Retrieves or sets the ending coordinates of the linear gradient. |
| [GradientStopCollection](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_lineargradientbrush_gradientstopcollection) | Retrieves the GradientStopCollection associated with this linear gradient brush. |
| [IsDisposed](https://developer.ninjatrader.com/docs/desktop/sharpdx_disposebase_isdisposed) | Gets a value indicating whether this instance is disposed. (Inherited from [SharpDX.DisposeBase](https://developer.ninjatrader.com/docs/desktop/sharpdx_disposebase)). |
| [Opacity](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_brush_opacity) | Gets or sets the degree of opacity of this brush. (Inherited from [Brush](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_brush)). |
| [StartPoint](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_lineargradientbrush_startpoint) | Retrieves or sets the starting coordinates of the linear gradient. |
| [Transform](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_brush_transform) | Gets or sets the transform applied to this brush. (Inherited from [Brush](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_brush)). |
