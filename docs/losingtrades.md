# LosingTrades

Source: https://developer.ninjatrader.com/docs/desktop/losingtrades

---

# LosingTrades


## [Definition](https://developer.ninjatrader.com/docs/desktop/losingtrades#definition)


A subcollection of **Trade** objects consisting of only the losing trades in a **TradeCollection**. You can access a trade object by providing an index value. Trades are indexed sequentially meaning the oldest trade taken in a strategy will be at an index value of zero. The most recent trade taken will be at an index value of the total trades in the collection minus 1.


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/losingtrades#methods-and-properties)


| --- |
| [Count](https://developer.ninjatrader.com/docs/desktop/tradescount) | An **int** value representing the number of trades in the collection |
| [GetTrades()](https://developer.ninjatrader.com/docs/desktop/gettrades) | Gets a **TradeCollection** object representing a specified position |
| [TradesPerformance](https://developer.ninjatrader.com/docs/desktop/tradesperformance) | Gets a **TradesPerformance** object |


## [Syntax](https://developer.ninjatrader.com/docs/desktop/losingtrades#syntax)


`<tradecollection>.LosingTrades`


## [Examples](https://developer.ninjatrader.com/docs/desktop/losingtrades#examples)


```csharp
protected override void OnBarUpdate()
{
     // Accesses the first/last losing trade in the strategy (oldest trade is at index 0)
     // and prints out the profit as a percentage to the output window
     if (SystemPerformance.AllTrades.LosingTrades.Count > 1)
     {
         Trade lastTrade = SystemPerformance.AllTrades.LosingTrades[SystemPerformance.AllTrades.Count - 1];
         Trade firstTrade = SystemPerformance.AllTrades.LosingTrades[0];

         Print("The last losing trade's profit was " + lastTrade.ProfitPercent);
         Print("The first losing trade's profit was " + firstTrade.ProfitPercent);
     }
}
```
