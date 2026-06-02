# SortinoRatio

Source: https://developer.ninjatrader.com/docs/desktop/sortinoratio

---

# SortinoRatio


## [Definition](https://developer.ninjatrader.com/docs/desktop/sortinoratio#definition)


Returns the Sortino ratio using a **risk free return**.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/sortinoratio#property-value)


A **double** value that represents the Sortino ratio using a risk free return.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/sortinoratio#syntax)


`<tradecollection>.TradesPerformance.SortinoRatio`


## [Examples](https://developer.ninjatrader.com/docs/desktop/sortinoratio#examples)


```csharp
protected override void OnBarUpdate()
{
     // Set a 0% risk free return
     SystemPerformance.AllTrades.TradesPerformance.RiskFreeReturn = 0;

     // Print out the Sortino ratio of all trades based on a zero risk free return
     Print("Sortino ratio is: " + SystemPerformance.AllTrades.TradesPerformance.SortinoRatio);
}
```
