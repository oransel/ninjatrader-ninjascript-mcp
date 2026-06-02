# CumProfit

Source: https://developer.ninjatrader.com/docs/desktop/cumprofit

---

# CumProfit


## [Definition](https://developer.ninjatrader.com/docs/desktop/cumprofit#definition)


Returns the cumulative profit of the collection.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/cumprofit#property-value)


A **double** value that represents the cumulative profit of the collection.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/cumprofit#syntax)


`<tradecollection>.TradesPerformance.<`tradesperformancevalues>.CumProfit`


## [Examples](https://developer.ninjatrader.com/docs/desktop/cumprofit#examples)


```csharp
// Print out the cumulative profit of all trades in currency
protected override void OnBarUpdate()
{
    // Print out the cumulative profit of all trades in currency
    Print("Average cumulative profit of all trades is: " + SystemPerformance.AllTrades.TradesPerformance.Currency.CumProfit);
}
```
