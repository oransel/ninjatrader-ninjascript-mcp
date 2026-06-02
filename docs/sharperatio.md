# SharpeRatio

Source: https://developer.ninjatrader.com/docs/desktop/sharperatio

---

# SharpeRatio


## [Definition](https://developer.ninjatrader.com/docs/desktop/sharperatio#definition)


Returns the Sharpe ratio using a **risk free return**.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/sharperatio#property-value)


A **double** value that represents the Sharpe ratio using a risk free return.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/sharperatio#syntax)


`<tradecollection>.TradesPerformance.SharpeRatio`


## [Examples](https://developer.ninjatrader.com/docs/desktop/sharperatio#examples)


```csharp
protected override void OnBarUpdate()
{
     // Set a 0% risk free return
     SystemPerformance.AllTrades.TradesPerformance.RiskFreeReturn = 0;

     // Print out the Sharpe ratio of all trades based on a zero risk free return
     Print("Sharpe ratio is: " + SystemPerformance.AllTrades.TradesPerformance.SharpeRatio);
}
```
