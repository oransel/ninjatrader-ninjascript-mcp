# IsTickReplay

Source: https://developer.ninjatrader.com/docs/desktop/istickreplay

---

# IsTickReplay


## [Definition](https://developer.ninjatrader.com/docs/desktop/istickreplay#definition)


Indicates if the bar series is using the **Tick Replay** data series property.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/istickreplay#property-value)


This property returns true if the bar series is using tick replay; otherwise, false. This property is read-only.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/istickreplay#syntax)


`Bars.IsTickReplay`
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


Warning: A Tick Replay indicator or strategy CANNOT use a **MarketDataType.Ask** or **MarketDataType.Bid** series. Please see [Developing for Tick Replay](https://developer.ninjatrader.com/docs/desktop/developing_for_tick_replay) for more information.


## [Examples](https://developer.ninjatrader.com/docs/desktop/istickreplay#examples)


```csharp
private double askPrice;
protected override void OnMarketData(MarketDataEventArgs marketDataUpdate)
{
    if(Bars.IsTickReplay)
    {
        // if using tick replay, get the current ask price associated with the tick
        askPrice = marketDataUpdate.Ask;
    }
    else // otherwise, get the real-time market data price during MarketDataType.Ask event
        askPrice = marketDataUpdate.MarketDataType == MarketDataType.Ask ? marketDataUpdate.Price : double.MinValue;

    // only print if a value is set
    if(askPrice != double.MinValue)
    {
        Print("ask price: " + askPrice);
    }
}
```
