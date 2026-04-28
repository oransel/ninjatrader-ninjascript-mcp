# TradeCollection

Source: https://developer.ninjatrader.com/docs/desktop/tradecollection

---

# TradeCollection


## [Definition](https://developer.ninjatrader.com/docs/desktop/tradecollection#definition)


A collection of **Trade** objects. You can access a trade object by providing an index value. Trades are indexed sequentially meaning the oldest trade taken in a strategy will be at an index value of zero. The most recent trade taken will be at an index value of the total trades in the collection minus 1.


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/tradecollection#methods-and-properties)


| --- |
| [TradesCount](https://developer.ninjatrader.com/docs/desktop/tradescount) | An **int** value representing the number of trades in the collection |
| [EvenTrades](https://developer.ninjatrader.com/docs/desktop/eventrades) | Gets a TradeCollection object of even trades |
| [GetTrades()](https://developer.ninjatrader.com/docs/desktop/gettrades) | Gets a TradeCollection object representing a specified position |
| [LosingTrades](https://developer.ninjatrader.com/docs/desktop/losingtrades) | Gets a TradeCollection object of losing trades |
| [TradesPerformance](https://developer.ninjatrader.com/docs/desktop/tradesperformance) | Gets a [TradesPerformance](https://developer.ninjatrader.com/docs/desktop/tradesperformance) object |
| [WinningTrades](https://developer.ninjatrader.com/docs/desktop/winningtrades) | Gets a TradeCollection object of winning trades |


## [Examples](https://developer.ninjatrader.com/docs/desktop/tradecollection#examples)


```csharp
protected override void OnBarUpdate()
{
   // Accesses the first/last trade in the strategy (oldest trade is at index 0)
   // and prints out the profit as a percentage to the output window
   if (SystemPerformance.AllTrades.Count > 1)
   {
       Trade lastTrade = SystemPerformance.AllTrades[SystemPerformance.AllTrades.Count - 1];
       Trade firstTrade = SystemPerformance.AllTrades[0];

       Print("The last trade profit is " + lastTrade.ProfitPercent);
       Print("The first trade profit is " + firstTrade.ProfitPercent);
   }
}
```


```csharp
protected override void OnBarUpdate()
{
   // Once the strategy has executed 20 trades loop through the losing trades
   // collection and print out the PnL on only long trades
   if (SystemPerformance.AllTrades.Count == 20)
   {
       Print("There are " + SystemPerformance.AllTrades.LosingTrades.Count + " losing trades.");
       foreach (Trade myTrade in SystemPerformance.AllTrades.LosingTrades)
       {
           if (myTrade.Entry.MarketPosition == MarketPosition.Long)
               Print(myTrade.ProfitCurrency);
       }
   }
}
```
