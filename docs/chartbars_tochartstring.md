# ToChartString()

Source: https://developer.ninjatrader.com/docs/desktop/chartbars_tochartstring

---

# ToChartString()


## [Definition](https://developer.ninjatrader.com/docs/desktop/chartbars_tochartstring#definition)


Returns a formatted string representing the **ChartBars.Properties.Label** property, **BarsPeriod** Value, and **BarsPeriodType** name.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


The property returned is dependent on a user configured **Data Series** property, and results may return differently than expected. See also **Bars.ToChartString()** for a return value which is not subject to user-defined variables.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/chartbars_tochartstring#syntax)


`ChartBars.ToChartString()`


## [Return Value](https://developer.ninjatrader.com/docs/desktop/chartbars_tochartstring#return-value)


A **string** value that represents the ChartBars label and configured bars period.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/chartbars_tochartstring#parameters)


This method does not accept any parameters.


## [Examples](https://developer.ninjatrader.com/docs/desktop/chartbars_tochartstring#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
   if (ChartBars != null)
     Print(ChartBars.ToChartString()); // My Favorite Instrument (1 Minute)
}
```
