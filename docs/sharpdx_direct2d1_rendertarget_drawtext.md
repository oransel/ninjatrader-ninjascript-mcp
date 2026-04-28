# SharpDX.Direct2D1.RenderTarget.DrawText()

Source: https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_rendertarget_drawtext

---

# SharpDX.Direct2D1.RenderTarget.DrawText()
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


Disclaimer: The **SharpDX SDK Reference** section was compiled from the official **SharpDX Documentation** and was NOT authored by NinjaTrader. The contents of this section are provided as-is and only cover a fraction of what is available from the SharpDX SDK. This page was intended only as a reference guide to help you get started with some of the 2D Graphics concepts used in the NinjaTrader.Custom assembly. Please refer to the official SharpDX Documentation for additional members not covered in this reference. For more seasoned graphic developers, the original MSDN **Direct2D1** and **DirectWrite** unmanaged API documentation can also be helpful for understanding the DirectX/Direct2D run-time environment. For NinjaScript development purposes, we document only essential members in the structure of this page.


## [Definition](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_rendertarget_drawtext#definition)


Draws the specified text using the format information provided by an **SharpDX.DirectWrite.TextFormat** object.


(See also **unmanaged API documentation**)
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This method doesn't return an error code if it fails.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_rendertarget_drawtext#method-return-value)


This method does not return a value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/sharpdx_direct2d1_rendertarget_drawtext#syntax)


`RenderTarget.DrawText(string text, TextFormat textFormat, RectangleF layoutRect, Brush defaultForegroundBrush)`


`RenderTarget.DrawText(string text, TextFormat textFormat, RectangleF layoutRect, Brush defaultForegroundBrush, DrawTextOptions options)`


`RenderTarget.DrawText(string text, TextFormat textFormat, RectangleF layoutRect, Brush defaultForegroundBrush, DrawTextOptions options, MeasuringMode measuringMode)`


`RenderTarget.DrawText(string text, int stringLength, TextFormat textFormat, RectangleF layoutRect, Brush defaultForegroundBrush, RenderTarget.DrawTextOptions options, MeasuringMode measuringMode)`


### Parameters


| Property | Description |
| --- | --- |
| `defaultForegroundBrush` | The **SharpDX.Direct2D1.Brush** used to paint the text. |
| `layoutRect` | A **SharpDX.RectangleF** which determines size and position of the area in which the text is drawn. |
| `measuringMode` | A **SharpDX.Direct2D1.MeasuringMode** value that indicates how glyph metrics are used to measure text when it is formatted. The default value is **DWRITE_MEASURING_MODE_NATURAL**. |
| `options` | A **SharpDX.Direct2D1.DrawTextOptions** value that indicates whether the text should be snapped to pixel boundaries and whether the text should be clipped to the layout rectangle. The default value is **None**, which indicates that text should be snapped to pixel boundaries and it should not be clipped to the layout rectangle. |
| `stringLength` | An **int** value which represents the number of characters in string. |
| `text` | A string reference to an array of Unicode characters to draw. |
| `textFormat` | A **SharpDX.DirectWrite.TextFormat** object that describes formatting details of the text to draw, such as the font, the font size, and flow direction. |
