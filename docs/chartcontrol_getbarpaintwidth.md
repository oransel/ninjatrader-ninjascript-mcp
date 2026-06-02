# GetBarPaintWidth()

Source: https://developer.ninjatrader.com/docs/desktop/chartcontrol_getbarpaintwidth

---

# GetBarPaintWidth()


## [Definition](https://developer.ninjatrader.com/docs/desktop/chartcontrol_getbarpaintwidth#definition)


Returns the width of the bars in the primary Bars object on the chart, in pixels.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/chartcontrol_getbarpaintwidth#method-return-value)


A double representing the pixel width of bars on the chart.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/chartcontrol_getbarpaintwidth#syntax)


`<chartcontrol>.GetBarPaintWidth(ChartBars chartBars)`


## [Method Parameters](https://developer.ninjatrader.com/docs/desktop/chartcontrol_getbarpaintwidth#method-parameters)


| --- |
| **chartBars** | A [ChartBars](https://developer.ninjatrader.com/docs/desktop/chartbars) object to measure |


## [Examples](https://developer.ninjatrader.com/docs/desktop/chartcontrol_getbarpaintwidth#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
   // Use BarsArray[0] to pass in a ChartBars object representing the primary Bars object on the chart
   double barPixelWidth = chartControl.GetBarPaintWidth(chartControl.BarsArray[0]);

   // Print the pixel width of bars painted on the chart
   Print(String.Format("Bars on the chart are {0} pixels wide", barPixelWidth));
}
```


In the image below, **GetBarPaintWidth()** reveals that the bars are being drawn 27 pixels wide on the chart:


![ChartControl_GetBarPaintWidth](https://cdn.sanity.io/images/1hlwceal/production/f5c388624347d7cf06b9a3a6b43d88d5d6f5df9a-531x431.png)
