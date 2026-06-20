# WinningTrades

Source: https://developer.ninjatrader.com/docs/desktop/winningtrades

---

# WinningTrades


## [Definition](https://developer.ninjatrader.com/docs/desktop/winningtrades#definition)


A subcollection of [Trade](https://developer.ninjatrader.com/docs/desktop/trade) objects consisting of only the winning trades in a [TradeCollection](https://developer.ninjatrader.com/docs/desktop/tradecollection). You can access a trade object by providing an index value. Trades are indexed sequentially meaning the oldest trade taken in a strategy will be at an index value of zero. The most recent trade taken will be at an index value of the total trades in the collection minus 1.


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/winningtrades#methods-and-properties)


| Method/Property | Description |
| --- | --- |
| [Count](https://developer.ninjatrader.com/docs/desktop/tradescount) | An int value representing the number of trades in the collection |
| [GetTrades()](https://developer.ninjatrader.com/docs/desktop/gettrades) | Gets a [TradeCollection](https://developer.ninjatrader.com/docs/desktop/tradecollection) object representing a specified position |
| [TradesPerformance](https://developer.ninjatrader.com/docs/desktop/tradesperformance) | Gets a [TradesPerformance](https://developer.ninjatrader.com/docs/desktop/tradesperformance) object |


## [Syntax](https://developer.ninjatrader.com/docs/desktop/winningtrades#syntax)


`<TradeCollection>.WinningTrades`


## [Examples](https://developer.ninjatrader.com/docs/desktop/winningtrades#examples)


```csharp
protected override void OnBarUpdate()
{
    // Accesses the first/last winning trade in the strategy (oldest trade is at index 0)
    // and prints out the profit as a percentage to the output window
    if (SystemPerformance.AllTrades.WinningTrades.Count > 1)
    {
        Trade lastTrade = SystemPerformance.AllTrades.WinningTrades[SystemPerformance.AllTrades.Count - 1];
        Trade firstTrade = SystemPerformance.AllTrades.WinningTrades[0];
 
        Print("The last winning trade's profit was " + lastTrade.ProfitPercent);
        Print("The first winning trade's profit was " + firstTrade.ProfitPercent);
    }
}
```
