# SharpDX.Direct2D1.LinearGradientBrushProperties

Source: https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_lineargradientbrushproperties

---

# SharpDX.Direct2D1.LinearGradientBrushProperties
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


Disclaimer: The **SharpDX SDK Reference** section was compiled from the official **SharpDX Documentation** and was NOT authored by NinjaTrader. The contents of this section are provided as-is and only cover a fraction of what is available from the SharpDX SDK. This page was intended only as a reference guide to help you get started with some of the 2D Graphics concepts used in the NinjaTrader.Custom assembly. Please refer to the official SharpDX Documentation for additional members not covered in this reference. For more seasoned graphic developers, the original MSDN **Direct2D1** and **DirectWrite** unmanaged API documentation can also be helpful for understanding the DirectX/Direct2D run-time environment. For NinjaScript development purposes, we document only essential members in the structure of this page.


## [Definition](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_lineargradientbrushproperties#definition)


Contains the starting point and endpoint of the gradient axis for an **LinearGradientBrush**.


(See also [unmanaged API documentation](https://msdn.microsoft.com/en-us/library/dd368128.aspx))


## [Syntax](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_lineargradientbrushproperties#syntax)


`struct LinearGradientBrushProperties`


## [Constructors](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_lineargradientbrushproperties#constructors)


| Constructor | Description |
| --- | --- |
| `new*LinearGradientBrushProperties()` | Initializes a new instance of the **LinearGradientBrushProperties** structure |


## [Properties](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_lineargradientbrushproperties#properties)


| Property | Description |
| --- | --- |
| **StartPoint** | A **SharpDX.Vector2** representing brush's coordinate space, the starting point of the gradient axis. |
| **EndPoint** | A **SharpDX.Vector2** representing the brush's coordinate space, the endpoint of the gradient axis. |
