# SharpDX.Direct2D1.Brush.Transform

Source: https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_brush_transform

---

# SharpDX.Direct2D1.Brush.Transform
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


Disclaimer: The **SharpDX SDK Reference** section was compiled from the official **SharpDX Documentation** and was NOT authored by NinjaTrader. The contents of this section are provided as-is and only cover a fraction of what is available from the SharpDX SDK. This page was intended only as a reference guide to help you get started with some of the 2D Graphics concepts used in the NinjaTrader.Custom assembly. Please refer to the official SharpDX Documentation for additional members not covered in this reference. For more seasoned graphic developers, the original MSDN **Direct2D1** and **DirectWrite** unmanaged API documentation can also be helpful for understanding the DirectX/Direct2D run-time environment. For NinjaScript development purposes, we document only essential members in the structure of this page.


## [Definition](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_brush_transform#definition)


Gets or sets the transform applied to this brush.


(See also [unmanaged API documentation](https://msdn.microsoft.com/en-us/library/dd371179(v=vs.85).aspx))


## [Note](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_brush_transform#note)
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


When the brush transform is the identity matrix, the brush appears in the same coordinate space as the render target in which it is drawn.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_brush_transform#property-value)


A **Matrix3x2** transform applied to this brush.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_brush_transform#syntax)


`<brush>.Transform`
