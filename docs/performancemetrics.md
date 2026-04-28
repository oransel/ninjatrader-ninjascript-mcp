# PerformanceMetrics

Source: https://developer.ninjatrader.com/docs/desktop/performancemetrics

---

# PerformanceMetrics


## [Definition](https://developer.ninjatrader.com/docs/desktop/performancemetrics#definition)


Returns a collection of custom **Performance Metrics**. These need to have been enabled in [Tools > Options > General](https://ninjatrader.com/support/helpGuides/nt8/NT%20HelpGuide%20English.html?general_section.htm) to be able to use them.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/performancemetrics#syntax)


`<tradecollection>.TradesPerformance.PerformanceMetrics`


## [Examples](https://developer.ninjatrader.com/docs/desktop/performancemetrics#examples)


```csharp
protected override void OnBarUpdate()
{
     // Print out the number of enabled custom Performance Metrics
     Print("Number of Performance Metrics: "
         + SystemPerformance.AllTrades.TradesPerformance.PerformanceMetrics.Length);

     // Find a the value of a specific custom Performance Metric named "MyPerformanceMetric"
     for (int i = 0; i < SystemPerformance.AllTrades.TradesPerformance.PerformanceMetrics.Length; i++)
     {
         if (SystemPerformance.AllTrades.TradesPerformance.PerformanceMetrics[i] is
               NinjaTrader.NinjaScript.PerformanceMetrics.MyPerformanceMetric)
         {
               Print((SystemPerformance.AllTrades.TradesPerformance.PerformanceMetrics[i] as
                   NinjaTrader.NinjaScript.PerformanceMetrics.MyPerformanceMetric).Values[0]);
         }
     }
}
```
