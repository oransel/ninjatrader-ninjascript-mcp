# ConvertFromHorizontalPixels

Source: https://developer.ninjatrader.com/docs/desktop/convertfromhorizontalpixels

---

# ConvertFromHorizontalPixels


## [Definition](https://developer.ninjatrader.com/docs/desktop/convertfromhorizontalpixels#definition)


Converts an x-axis pixel coordinate from device pixels to application pixels.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


For more information concerning the differences between application pixels and device pixels, please see the [Working with Pixel Coordinates](https://developer.ninjatrader.com/docs/desktop/working_with_pixel_coordinates).


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/convertfromhorizontalpixels#method-return-value)


A double representing an x-coordinate value in terms of application pixels.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/convertfromhorizontalpixels#syntax)


`ChartingExtensions.ConvertFromHorizontalPixels(this int x, PresentationSource target)`


`int.ConvertFromHorizontalPixels(PresentationSource target)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/convertfromhorizontalpixels#parameters)


| Parameter | Description |
| --- | --- |
| **x** | The horizontal int coordinates in device pixels to convert. |
| **target** | The [PresentationSource](https://msdn.microsoft.com/en-us/library/system.windows.presentationsource(v=vs.110).aspx) representing the display surface used for the conversion. Note: For Charts, see [ChartControl.PresentationSource](https://developer.ninjatrader.com/docs/desktop/presentationsource). |


## [Examples](https://developer.ninjatrader.com/docs/desktop/convertfromhorizontalpixels#examples)


```csharp
int applicationPixelX;

protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
    // Obtain the application-pixel coordinate corresponding to a device-pixel X value of 500
    applicationPixelX = ChartingExtensions.ConvertFromHorizontalPixels(500, ChartControl.PresentationSource);
}
```
