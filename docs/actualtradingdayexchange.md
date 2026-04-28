# ActualTradingDayExchange

Source: https://developer.ninjatrader.com/docs/desktop/actualtradingdayexchange

---

# ActualTradingDayExchange


## [Definition](https://developer.ninjatrader.com/docs/desktop/actualtradingdayexchange#definition)


Obtains the date of a trading session defined by the exchange.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


- In order to obtain historical ActualTradingDayExchange information, you must call [GetNextSession](https://developer.ninjatrader.com/docs/desktop/getnextsession) from a stored SessionIterator object.
- The calculated value may differ from the current date as some trading sessions will begin before the actual calendar date changes. For example, the "CME US Index Futures ETH" [actual session](https://developer.ninjatrader.com/docs/desktop/accumulation_distribution_adl) started on 3/30/2015 at 5:00PM Central Time, however the actual exchange trading day would be considered 3/31/2015 12:00:00AM.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/actualtradingdayexchange#property-value)


A DateTime structure that represents the trading day.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/actualtradingdayexchange#syntax)


`SessionIterator.ActualTradingDayExchange`


## [Example](https://developer.ninjatrader.com/docs/desktop/actualtradingdayexchange#example)


```csharp
SessionIterator sessionIterator;

protected override void OnStateChange()
{
    if (State == State.Historical)
    {
        sessionIterator = new SessionIterator(Bars);
    }
}

protected override void OnBarUpdate()
{
    // on new bars session, find the next trading session
    if (Bars.IsFirstBarOfSession)
    {
        // use the current bar time to calculate the next session
        sessionIterator.GetNextSession(Time[0], true);

        Print("The current exchange trading day is " + sessionIterator.ActualTradingDayExchange);
    }
}
```
