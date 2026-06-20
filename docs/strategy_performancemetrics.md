# PerformanceMetrics

Source: https://developer.ninjatrader.com/docs/desktop/strategy_performancemetrics

---

# PerformanceMetrics


## [Definition](https://developer.ninjatrader.com/docs/desktop/strategy_performancemetrics#definition)


Holds an array of **PerformanceMetrics** objects that represent custom metrics that can be used for strategy calculations.


Index value is based on the array of Bars objects added via the **AddPerformanceMetric** method.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/strategy_performancemetrics#property-value)


An array of **PerformanceMetrics** objects.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/strategy_performancemetrics#syntax)


`PerformanceMetrics[int index]`


## [Examples](https://developer.ninjatrader.com/docs/desktop/strategy_performancemetrics#examples)


```csharp
// Define a new SampleCumProfit object
NinjaTrader.NinjaScript.PerformanceMetrics.SampleCumProfit myProfit;
protected override void OnStateChange()
{
   if (State == State.Configure)
   {
     // Instantiate myProfit to a new instance of SampleCumProfit
     myProfit = new NinjaTrader.NinjaScript.PerformanceMetrics.SampleCumProfit();
      
     // Use AddPerformanceMetric to add myProfit to the strategy
     AddPerformanceMetric(myProfit);
   }
}
protected override void OnBarUpdate()
{
   // Print a string representing the Type of the performance metric at Index 0 of the PerformanceMetrics collection
   Print(PerformanceMetrics[0]);
}
```
