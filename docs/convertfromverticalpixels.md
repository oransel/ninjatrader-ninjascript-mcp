# ConvertFromVerticalPixels

Source: https://developer.ninjatrader.com/docs/desktop/convertfromverticalpixels

---

# ConvertFromVerticalPixels


## [Definition](https://developer.ninjatrader.com/docs/desktop/convertfromverticalpixels#definition)


Converts a y-axis pixel coordinate from device pixels to application pixels.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


For more information concerning the differences between application pixels and device pixels, please see the [Working with Pixel Coordinates](https://developer.ninjatrader.com/docs/desktop/working_with_pixel_coordinates).


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/convertfromverticalpixels#method-return-value)


A double representing a y-coordinate value in terms of application pixels.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/convertfromverticalpixels#syntax)


`ChartingExtensions.ConvertFromVerticalPixels(this int x, PresentationSource target)`


`<int>.ConvertFromVerticalPixels(PresentationSource target)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/convertfromverticalpixels#parameters)


| --- |
| x | target |
| The vertical int coordinates in device pixels to convert | The [PresenationSource](https://msdn.microsoft.com/en-us/library/system.windows.presentationsource(v=vs.110).aspx) representing the display surface used for the conversion. Note: For Charts, see [ChartControl.PresentationSource](https://developer.ninjatrader.com/docs/desktop/presentationsource). |


## [Examples](https://developer.ninjatrader.com/docs/desktop/convertfromverticalpixels#examples)


```csharp
int applicationPixelY;

protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
    // Obtain the application-pixel coordinate corresponding to a device-pixel Y value of 500
    applicationPixelY = ChartingExtensions.ConvertFromVerticalPixels(500, ChartControl.PresentationSource);
}
```
