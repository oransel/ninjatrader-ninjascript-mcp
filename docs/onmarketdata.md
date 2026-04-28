# OnMarketData()

Source: https://developer.ninjatrader.com/docs/desktop/onmarketdata

---

# OnMarketData()


## [Definition](https://developer.ninjatrader.com/docs/desktop/onmarketdata#definition)


An event driven method which is called and guaranteed to be in the correct sequence for every change in level one market data for the underlying instrument. **OnMarketData()** can include but is not limited to the bid, ask, last price and volume.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


- This is a real-time data stream and can be CPU intensive if your program code is compute intensive (not optimal).
- By default, this method is not called on historical data (backtest), however it can be called historically by using [TickReplay](https://developer.ninjatrader.com/docs/desktop/developing_for_tick_replay).
- If used with [TickReplay](https://developer.ninjatrader.com/docs/desktop/developing_for_tick_replay), please keep in mind Tick Replay ONLY replays the Last market data event, and only stores the best inside bid/ask price at the time of the last trade event. You can think of this as the equivalent of the bid/ask price at the time a trade was reported. As such, historical bid/ask market data events (i.e., bid/ask volume) DO NOT work with Tick Replay. To obtain those values, you need to use a [historical bid/ask series](https://developer.ninjatrader.com/docs/desktop/using_historical_bid_ask_serie) separately from TickReplay through **OnBarUpdate()**. More information can be found under [Developing for Tick Replay](https://developer.ninjatrader.com/docs/desktop/developing_for_tick_replay).
- With [multi-time frame and instrument strategies](https://developer.ninjatrader.com/docs/desktop/multi_time_frame_instruments), a subscription will be created on all bars series added in your indicator or strategy (even if the instrument is the same). The market data subscription behavior occurs both in real-time and during [TickReplay](https://developer.ninjatrader.com/docs/desktop/developing_for_tick_replay) historical.
- Do not leave an unused **OnMarketData()** method declared in your NinjaScript object. This will unnecessarily attach a data stream to your strategy which uses unnecessary CPU cycles.
- Should you wish to run comparisons against prior values you will need to store and update local variables to track the relevant values.
- The **OnMarketData()** method is expected to be called after [OnBarUpdate()](https://developer.ninjatrader.com/docs/desktop/onbarupdate).


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/onmarketdata#method-return-value)


This method does not return a value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/onmarketdata#syntax)


You must override the method in your strategy or indicator with the following syntax.


**protected override void OnMarketData(MarketDataEventArgs marketDataUpdate)**
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


The NinjaScript code wizards can automatically generate the method syntax for you when creating a new script.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/onmarketdata#parameters)


| Parameter | Description |
| --- | --- |
| **marketDataUpdate** | [MarketDataEventArgs](https://developer.ninjatrader.com/docs/desktop/marketdataeventargs) representing the recent change in market data |


## [Examples](https://developer.ninjatrader.com/docs/desktop/onmarketdata#examples)


```csharp
protected override void OnMarketData(MarketDataEventArgs marketDataUpdate)
{
     // Print some data to the Output window
     if (marketDataUpdate.MarketDataType == MarketDataType.Last)
           Print(string.Format("Last = {0} {1} ", marketDataUpdate.Price, marketDataUpdate.Volume));
     else if (marketDataUpdate.MarketDataType == MarketDataType.Ask)
         Print(string.Format("Ask = {0} {1} ", marketDataUpdate.Price, marketDataUpdate.Volume));
     else if (marketDataUpdate.MarketDataType == MarketDataType.Bid)
         Print(string.Format("Bid = {0} {1}", marketDataUpdate.Price, marketDataUpdate.Volume));
}
```
