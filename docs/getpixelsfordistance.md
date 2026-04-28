# GetPixelsForDistance()

Source: https://developer.ninjatrader.com/docs/desktop/getpixelsfordistance

---

# GetPixelsForDistance()


## [Definition](https://developer.ninjatrader.com/docs/desktop/getpixelsfordistance#definition)


Returns the number of device pixels between the value passed to the method representing a series point value on the chart scale.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/getpixelsfordistance#method-return-value)


A float representing the number of pixels between a value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/getpixelsfordistance#syntax)


`<chartscale>.GetPixelsForDistance(double distance)`


## [Method Parameters](https://developer.ninjatrader.com/docs/desktop/getpixelsfordistance#method-parameters)


| --- |
| distance | A **double** value representing the distance in points to be measured |


## [Examples](https://developer.ninjatrader.com/docs/desktop/getpixelsfordistance#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
   // the number of pixels between the point value passed as a distance to the method
   float pixelForDistance = chartScale.GetPixelsForDistance(0.25);

   Print("pixelForDistance: " + pixelForDistance); //20 pixels per every 1 tick on the chart scale

}
```


In the image below, we pass a value of 1 for the distance, which tells us there are 76 pixels for every 1 point on the ES 06-15 chart scale.


![GetPixelsForDistance](https://cdn.sanity.io/images/1hlwceal/production/23f135c9e1f379b4fbe13ce31ed0089a3915309c-535x433.png)
