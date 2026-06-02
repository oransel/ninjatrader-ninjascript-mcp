# ProfitPerMonth

Source: https://developer.ninjatrader.com/docs/desktop/profitpermonth

---

# ProfitPerMonth


## [Definition](https://developer.ninjatrader.com/docs/desktop/profitpermonth#definition)


Returns the profit per month of the collection. This value is always returned as a percentage.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/profitpermonth#property-value)


A **double** value that represents the profit per month of the collection as a percentage.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/profitpermonth#syntax)


`<tradecollection>.TradesPerformance.<tradesperformancevalues>.ProfitPerMonth`


## [Examples](https://developer.ninjatrader.com/docs/desktop/profitpermonth#examples)


```csharp
protected override void OnBarUpdate()
{
     // Print out the profit per month of all trades
     Print("Profit per month of all trades is: " + SystemPerformance.AllTrades.TradesPerformance.Currency.ProfitPerMonth);
}
```
