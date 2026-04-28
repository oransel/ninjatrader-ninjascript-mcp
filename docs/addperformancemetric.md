# AddPerformanceMetric()

Source: https://developer.ninjatrader.com/docs/desktop/addperformancemetric

---

# AddPerformanceMetric()


## [Definition](https://developer.ninjatrader.com/docs/desktop/addperformancemetric#definition)


Adds an instance of custom **Performance Metric** to a strategy used in strategy calculations.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/addperformancemetric#method-return-value)


This method does not return a value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/addperformancemetric#syntax)


`AddPerformanceMetric(PerformanceMetricBase performanceMetric)`
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


This method should ONLY be called from the `OnStateChange()` method during State.Configure


## [Parameters](https://developer.ninjatrader.com/docs/desktop/addperformancemetric#parameters)


| --- |
| performanceMetric | The performance metric object to be added |


## [Examples](https://developer.ninjatrader.com/docs/desktop/addperformancemetric#examples)


```csharp
protected override void OnStateChange()
{
     if (State == State.Configure)
     {
         AddPerformanceMetric(new NinjaTrader.NinjaScript.PerformanceMetrics.SampleCumProfit());
     }
}
```
