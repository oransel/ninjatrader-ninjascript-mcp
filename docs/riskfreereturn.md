# RiskFreeReturn

Source: https://developer.ninjatrader.com/docs/desktop/riskfreereturn

---

# RiskFreeReturn


## [Definition](https://developer.ninjatrader.com/docs/desktop/riskfreereturn#definition)


The risk free return used in calculations of **Sharpe** and **Sortino** ratios.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/riskfreereturn#property-value)


A **double** value that represents the risk free return.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/riskfreereturn#syntax)


`<tradecollection>.TradesPerformance.RiskFreeReturn`


## [Examples](https://developer.ninjatrader.com/docs/desktop/riskfreereturn#examples)


```csharp
protected override void OnBarUpdate()
{
     // Set a 3.5% risk free return
     SystemPerformance.AllTrades.TradesPerformance.RiskFreeReturn = 0.035;

     // Print out the Sharpe ratio of all trades based on a 3.5% risk free return
     Print("Sharpe ratio is: " + SystemPerformance.AllTrades.TradesPerformance.SharpeRatio);
}
```
