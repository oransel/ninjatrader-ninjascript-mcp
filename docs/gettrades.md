# GetTrades()

Source: https://developer.ninjatrader.com/docs/desktop/gettrades

---

# GetTrades()


## [Definition](https://developer.ninjatrader.com/docs/desktop/gettrades#definition)


Returns a **TradeCollection** object representing all trades that make up the specified position.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/gettrades#method-return-value)


A **TradeCollection** object.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/gettrades#syntax)


`<tradecollection>.GetTrades(string instrument, string entrySignalName, int instance)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/gettrades#parameters)


| --- |
| **instrument** | An instrument name such as "MSFT" |
| **entrySignalName** | The name of your entry signal |
| **instance** | The occurrence to check for (1 is the most recent, 2 is the 2nd most recent position, etc...) |


## [Examples](https://developer.ninjatrader.com/docs/desktop/gettrades#examples)


```csharp
protected override void OnBarUpdate()
{
     TradeCollection myTrades = SystemPerformance.AllTrades.GetTrades("MSFT", "myEntrySignal", 1);
     Print("The last position was comprised of " + myTrades.Count + " trades.");
}
```
