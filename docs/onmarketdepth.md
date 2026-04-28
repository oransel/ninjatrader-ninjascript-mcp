# OnMarketDepth()

Source: https://developer.ninjatrader.com/docs/desktop/onmarketdepth

---

# OnMarketDepth()


## [Definition](https://developer.ninjatrader.com/docs/desktop/onmarketdepth#definition)


An event driven method which is called and guaranteed to be in the correct sequence for every change in level two market data (market depth) for the underlying instrument. The **OnMarketDepth()** method can be used to build your own level two book.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


- This is a real-time data stream and can be CPU intensive if your program code is compute intensive (not optimal)
- This method is not called on historical data (backtest)


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/onmarketdepth#method-return-value)


This method does not return a value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/onmarketdepth#syntax)


You must override the method in your strategy or indicator with the following syntax:


`protected override void OnMarketDepth(MarketDepthEventArgs marketDepthUpdate)`
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


The NinjaScript code wizards can automatically generate the method syntax for you when creating a new script.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/onmarketdepth#parameters)


| --- |
| marketDepthUpdate | **MarketDepthEventArgs** representing the recent change in market data |


## [Examples](https://developer.ninjatrader.com/docs/desktop/onmarketdepth#examples)


```csharp
protected override void OnMarketDepth(MarketDepthEventArgs marketDepthUpdate)
{
     // Print some data to the Output window
     if (marketDepthUpdate.MarketDataType == MarketDataType.Ask && marketDepthUpdate.Operation == Operation.Update)
         Print(string.Format("The most recent ask change is {0} {1}", marketDepthUpdate.Price, marketDepthUpdate.Volume));
}
```

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


- - With [multi-time frame and instrument strategies](https://developer.ninjatrader.com/docs/desktop/multi_time_frame_instruments), **OnMarketDepth** will be called for all unique instruments in your strategy. Use the [BarsInProgress](https://developer.ninjatrader.com/docs/desktop/barsinprogress) to filter the **OnMarketDepth()** method for a specific instrument. (BarsInProgress will return the first BarsInProgress series that matches the instrument for the event)
- - Do not leave an unused **OnMarketDepth()** method declared in your NinjaScript object. This will unnecessarily attach a data stream to your strategy which uses unnecessary CPU cycles.
- - Should you wish to run comparisons against prior values you will need to store and update local variables to track the relevant values.
- - With NinjaTrader being multi-threaded, you should not rely on any particular sequence of events like **OnMarketDepth()** always being called before **OnMarketData()** or vice versa.
