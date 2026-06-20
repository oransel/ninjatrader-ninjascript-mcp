# BarsPeriod

Source: https://developer.ninjatrader.com/docs/desktop/chartcontrol_barsperiod

---

# BarsPeriod


## [Definition](https://developer.ninjatrader.com/docs/desktop/chartcontrol_barsperiod#definition)


Provides the period (interval) used for the primary **Bars** object on the chart.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/chartcontrol_barsperiod#property-value)


A **NinjaTrader.Data.BarsPeriod** object containing information on the period used by the **Bars** object on the chart.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/chartcontrol_barsperiod#syntax)


`<chartcontrol>.BarsPeriod`


## [Examples](https://developer.ninjatrader.com/docs/desktop/chartcontrol_barsperiod#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
   BarsPeriod period = chartControl.BarsPeriod;
 
   // Print the period (interval) of the Bars object on the chart
   Print(period);
}
```


Based on the image below, **BarsPeriod** confirms that the primary **Bars** object on the chart is configured to a 5-minute interval.


![ChartControl_BarsPeriod](https://cdn.sanity.io/images/1hlwceal/production/676ace86d5b9ad2338dfbc22509291da8f9d517a-531x431.png)
