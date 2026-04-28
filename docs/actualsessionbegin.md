# ActualSessionBegin

Source: https://developer.ninjatrader.com/docs/desktop/actualsessionbegin

---

# ActualSessionBegin


## [Definition](https://developer.ninjatrader.com/docs/desktop/actualsessionbegin#definition)


Obtains the sessions start date and start time converted to the user's configured Time Zone.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


In order to obtain historical ActualSessionBegin information, you must call [GetNextSession](https://developer.ninjatrader.com/docs/desktop/getnextsession) from a stored SessionIterator object.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/actualsessionbegin#property-value)


A **DateTime** structure that represents beginning of a trading session.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/actualsessionbegin#syntax)


`SessionIterator.ActualSessionBegin`


## [Example](https://developer.ninjatrader.com/docs/desktop/actualsessionbegin#example)


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

        Print("The current session start time is " + sessionIterator.ActualSessionBegin);
    }
}
```
