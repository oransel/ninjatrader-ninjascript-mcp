# EvenTrades

Source: https://developer.ninjatrader.com/docs/desktop/eventrades

---

# EvenTrades


## [Definition](https://developer.ninjatrader.com/docs/desktop/eventrades#definition)


A subcollection of **Trade** objects consisting of only the non-winning and non-losing trades in a **TradeCollection**.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


You can access a trade object by providing an index value. Trades are indexed sequentially meaning the oldest trade taken in a strategy will be at an index value of zero. The most recent trade taken will be at an index value of the total trades in the collection minus 1.


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/eventrades#methods-and-properties)


| Method/Property | Description |
| --- | --- |
| [Count](https://developer.ninjatrader.com/docs/desktop/tradescount) | An **int** value representing the number of trades in the collection |
| [GetTrades()](https://developer.ninjatrader.com/docs/desktop/gettrades) | Gets a **TradeCollection** object representing a specified position |
| [TradesPerformance](https://developer.ninjatrader.com/docs/desktop/tradesperformance) | Gets a **TradesPerformance** object |


## [Syntax](https://developer.ninjatrader.com/docs/desktop/eventrades#syntax)


`<tradecollection>.EvenTrades`


## [Examples](https://developer.ninjatrader.com/docs/desktop/eventrades#examples)


```csharp
protected override void OnBarUpdate()
{
     // Accesses the first/last losing trade in the strategy (oldest trade is at index 0)
     // and prints out the quantity NinjaScript Output window
     if (SystemPerformance.AllTrades.EvenTrades.Count > 1)
     {
         Trade lastTrade = SystemPerformance.AllTrades.EvenTrades[SystemPerformance.AllTrades.Count - 1];
         Trade firstTrade = SystemPerformance.AllTrades.EvenTrades[0];

         Print("The last even trade's quantity was " + lastTrade.Quantity);
         Print("The first even trade's quantity was " + firstTrade.Quantity);
     }
}
```
