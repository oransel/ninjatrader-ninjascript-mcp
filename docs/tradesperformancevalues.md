# TradesPerformanceValues

Source: https://developer.ninjatrader.com/docs/desktop/tradesperformancevalues

---

# TradesPerformanceValues


## [Definition](https://developer.ninjatrader.com/docs/desktop/tradesperformancevalues#definition)


Performance values of a **collection** of **Trade** objects.


- Currency and Point based calculations are per trade
- Percent based calculations are per traded unit


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/tradesperformancevalues#methods-and-properties)


| --- |
| **AverageEtd** | A **double** value representing avg end trade draw down |
| **AverageMae** | A **double** value representing avg maximum adverse excursion |
| **AverageMfe** | A **double** value representing avg maximum favorable excursion |
| **AverageProfit** | A **double** value representing avg profit |
| **CumProfit** | A **double** value representing cumulative profit (percent is compounded) |
| **Drawdown** | A **double** value representing draw down |
| **LargestLoser** | A **double** value representing largest loss |
| **LargestWinner** | A **double** value representing largest gain |
| **ProfitPerMonth** | A **double** value representing profit per month always as a percent |
| **StdDev** | A **double** value representing standard deviation on a per unit basis |
| **Turnaround** | A **double** value representing the turnaround |
| **Ulcer** | A **double** value representing the Ulcer value |


## [Examples](https://developer.ninjatrader.com/docs/desktop/tradesperformancevalues#examples)


```csharp
protected override void OnBarUpdate()
{
     // If the profit on real-time trades is > $1000 stop trading
     if (SystemPerformance.RealTimeTrades.TradesPerformance.Currency.CumProfit > 1000)
          return;
}
```
