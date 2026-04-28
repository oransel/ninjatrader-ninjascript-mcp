# MinValue

Source: https://developer.ninjatrader.com/docs/desktop/chartscale_minvalue

---

# MinValue


## [Definition](https://developer.ninjatrader.com/docs/desktop/chartscale_minvalue#definition)


The lowest rendered value on the chart scale.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/chartscale_minvalue#property-value)


A **double** value representing the lowest value on the chart scale as a y value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/chartscale_minvalue#syntax)


`<chartscale>.MinValue`


## [Examples](https://developer.ninjatrader.com/docs/desktop/chartscale_minvalue#examples)
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


In the image below, the lowest value displayed as text on the y-axis reads 2102.50, however as you can see, there are a few pixels on the chart scale below this tick. The absolute rendered MinValue on the chart scale is calculated as 2102.29.


![MinValue](https://cdn.sanity.io/images/1hlwceal/production/c24f166f85e2229c5ad6ed5324a209894e15e52a-535x433.png)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
   // the minimum value of the chart scale
   double minValue   = chartScale.MinValue;

   Print("minValue: " + minValue);
}
```
