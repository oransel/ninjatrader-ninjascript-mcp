# GetTradingDayBeginLocal()

Source: https://developer.ninjatrader.com/docs/desktop/gettradingdaybeginlocal

---

# GetTradingDayBeginLocal()


## [Definition](https://developer.ninjatrader.com/docs/desktop/gettradingdaybeginlocal#definition)


Converts the trading day begin time from the exchange timezone to local time, and returns a DateTime object in the local timezone. The **ActualTradingDayExchange** property can be passed into **GetTradingDayBeginLocal()** for a quick timezone conversion.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/gettradingdaybeginlocal#property-value)


A DateTime object representing the exchange-based trading day begin time converted to local time.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/gettradingdaybeginlocal#syntax)


`<sessioniterator>.GetTradingDayBeginLocal(DateTime tradingDayExchange)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/gettradingdaybeginlocal#parameters)


| --- |
| tradingDayExchange | The DateTime value used to calculate the trading day. |


## [Examples](https://developer.ninjatrader.com/docs/desktop/gettradingdaybeginlocal#examples)


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
    // Only process strategy logic starting three hours after trading begins at the exchange
    if (Core.Globals.Now >= sessionIterator.GetTradingDayBeginLocal(sessionIterator.ActualTradingDayExchange).AddHours(3))
    {
        // Strategy logic here
    }
}
```
