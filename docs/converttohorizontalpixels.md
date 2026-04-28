# ConvertToHorizontalPixels

Source: https://developer.ninjatrader.com/docs/desktop/converttohorizontalpixels

---

# ConvertToHorizontalPixels


## [Definition](https://developer.ninjatrader.com/docs/desktop/converttohorizontalpixels#definition)


Converts an x-axis pixel coordinate from application pixels to device pixels.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


For more information concerning the differences between application pixels and device pixels, please see the [Working with Pixel Coordinates](https://developer.ninjatrader.com/docs/desktop/working_with_pixel_coordinates).


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/converttohorizontalpixels#method-return-value)


An int representing an x-coordinate value in terms of device pixels.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/converttohorizontalpixels#syntax)


`ChartingExtensions.ConvertToHorizontalPixels(this double x, PresentationSource target)`


`<double>.ConvertToHorizontalPixels(PresentationSource target)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/converttohorizontalpixels#parameters)


| --- |
| **x** | The horizontal double coordinates in application pixels to convert |
| **target** | The [PresenationSource](https://msdn.microsoft.com/en-us/library/system.windows.presentationsource(v=vs.110).aspx) representing the display surface used for the conversion.
Note: For Charts, see [ChartControl.PresentationSource](https://developer.ninjatrader.com/docs/desktop/presentationsource). |


## [Examples](https://developer.ninjatrader.com/docs/desktop/converttohorizontalpixels#examples)


```csharp
int devicePixelX;

protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
    // Obtain the device-pixel coordinate corresponding to an application pixel X-value of 500
    devicePixelX = ChartingExtensions.ConvertToHorizontalPixels(500, ChartControl.PresentationSource);
}
```
