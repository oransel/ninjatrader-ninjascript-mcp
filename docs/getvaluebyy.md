# GetValueByY()

Source: https://developer.ninjatrader.com/docs/desktop/getvaluebyy

---

# GetValueByY()


## [Definition](https://developer.ninjatrader.com/docs/desktop/getvaluebyy#definition)


Returns the series value on the chart scale determined by a y pixel coordinate on the chart.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/getvaluebyy#method-return-value)


A **double** value representing a series value on the chart scale. This is normally a price value, but can represent indicator plot values as well.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/getvaluebyy#syntax)


`<chartscale>.GetValueByY(float y)`


## [Method Parameters](https://developer.ninjatrader.com/docs/desktop/getvaluebyy#method-parameters)


| --- |
| **y** | A float value representing a pixel coordinate on the chart scale |


## [Examples](https://developer.ninjatrader.com/docs/desktop/getvaluebyy#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
   // the price value of the pixel coordinate passed in the method
   double valueByY =   chartScale.GetValueByY(1);

   Print("valueByY: " + valueByY); //2106.19693333
}
```


In the image below, we pass a value of 1 for the y value, which tells us the pixel coordinate of 1 is located at a price of 2106.19 on the chart scale.


![getvaluebyY](https://cdn.sanity.io/images/1hlwceal/production/c6bfc1f09add776095242528ac133bb5de245be2-535x433.png)
