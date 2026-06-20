# ToChartString()

Source: https://developer.ninjatrader.com/docs/desktop/tochartstring

---

# ToChartString()


## [Definition](https://developer.ninjatrader.com/docs/desktop/tochartstring#definition)


Returns the bars series as a formatted string, including the **Instrument.FullName**, **BarsPeriod** Value, and **BarsPeriodType** name.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


To obtain a return value which matches the user configured **ChartBars Label property**, please see the **ChartBars.ToChartString()** method.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/tochartstring#syntax)


`Bars.ToChartString()`


## [Return Value](https://developer.ninjatrader.com/docs/desktop/tochartstring#return-value)


A **string** value that represents the bars series.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/tochartstring#parameters)


This method does not accept any parameters.


## [Examples](https://developer.ninjatrader.com/docs/desktop/tochartstring#examples)


```csharp
protected override void OnBarUpdate()
{
   // print the chart string on start up
   if(CurrentBar == 0)
     Print(Bars.ToChartString()); // ES 09-15 (60 Minute)      
}
```
