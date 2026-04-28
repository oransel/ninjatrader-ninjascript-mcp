# GetTradingDayEndLocal()

Source: https://developer.ninjatrader.com/docs/desktop/gettradingdayendlocal

---

# GetTradingDayEndLocal()


## [Definition](https://developer.ninjatrader.com/docs/desktop/gettradingdayendlocal#definition)


Converts the trading day end time from the exchange timezone to local time, and returns a DateTime object in the local timezone. The **ActualTradingDayExchange** property can be passed into **GetTradingDayEndLocal()** for a quick timezone conversion.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/gettradingdayendlocal#property-value)


A DateTime object representing the exchange-based trading day end time converted to local time.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/gettradingdayendlocal#syntax)


`<sessioniterator>.GetTradingDayEndLocal(DateTime tradingDayExchange)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/gettradingdayendlocal#parameters)


| --- |
| tradingDayExchange | The DateTime value used to calculate the trading day. |


## [Examples](https://developer.ninjatrader.com/docs/desktop/gettradingdayendlocal#examples)


```csharp
private SessionIterator sessionIterator;
protected override void OnStateChange()
{
    if (State == State.DataLoaded)
    {
        //stores the sessions once bars are ready, but before OnBarUpdate is called
        sessionIterator = new SessionIterator(Bars);
    }
}
protected override void OnBarUpdate()
{
    // Only process strategy logic up until three hours prior to the end of the trading day at the exchange
    if (Core.Globals.Now <= sessionIterator.GetTradingDayEndLocal(sessionIterator.ActualTradingDayExchange).AddHours(-3))
    {
        // Strategy logic here
    }
}
```
