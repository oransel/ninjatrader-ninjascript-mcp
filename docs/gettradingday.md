# GetTradingDay()

Source: https://developer.ninjatrader.com/docs/desktop/gettradingday

---

# GetTradingDay()


## [Definition](https://developer.ninjatrader.com/docs/desktop/gettradingday#definition)


Returns the actual trading date based on the exchange, calculated from a DateTime object passed with the local time. **GetTradingDay()** calls **CalculateTradingDay()** on a custom **SessionIterator** object created by passing in a **Bars** object as an argument.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


Warning: This method can ONLY be called when a **SessionIterator** was created with a 'Bars' parameter.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/gettradingday#property-value)


A **DateTime** object representing the [ActualTradingDayExchange](https://developer.ninjatrader.com/docs/desktop/actualtradingdayexchange).


## [Syntax](https://developer.ninjatrader.com/docs/desktop/gettradingday#syntax)


`<sessioniterator>.GetTradingDay(DateTime timeLocal)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/gettradingday#parameters)


| --- |
| timeLocal | The **DateTime** value used to calculate the next trading day. |


## [Examples](https://developer.ninjatrader.com/docs/desktop/gettradingday#examples)


```csharp
// Declare a new custom SessionIterator
SessionIterator mySessionIterator;

protected override void OnStateChange()
{
    if (State == State.Historical)
    {
        // Instantiate mySessionIterator once in State.Configure
        mySessionIterator = new SessionIterator(BarsArray[0]);
    }
}

protected override void OnBarUpdate()
{
    // Obtain the ActualTradingDayExchange value for mySessionIterator, based on today's date
    Print(mySessionIterator.GetTradingDay(DateTime.Now).ToString());
}
```
