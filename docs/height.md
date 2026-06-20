# Height

Source: https://developer.ninjatrader.com/docs/desktop/height

---

# Height


## [Definition](https://developer.ninjatrader.com/docs/desktop/height#definition)


Indicates the overall distance (from top to bottom) of the chart scale.


## [Note](https://developer.ninjatrader.com/docs/desktop/height#note)
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Height does not return its value in terms of device pixels. However, using **Height.ConvertToVerticalPixels** or **Height.ConvertToHorizontalPixels** will convert the Height value to device pixels. Alternatively, **RenderTarget.PixelSize.Height** or **ChartPanel.H** will also provide the height in terms of device pixels.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/height#property-value)


A **double** value representing the height of the chart scale.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/height#syntax)


`<chartscale>.Height`


## [Examples](https://developer.ninjatrader.com/docs/desktop/height#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
   // the height of the entire chart scale
   double   height       = chartScale.Height;
   Print("the height of the chart scale is: " + height);  
}
```


In the image below, the entire height of the chart scale is represented by the blue line which is calculated at 300 pixels.


![Height](https://cdn.sanity.io/images/1hlwceal/production/ea66e5b40f1ce3b997dba05b76fc0e86cfff9151-535x433.png)
