# ActualSessionEnd

Source: https://developer.ninjatrader.com/docs/desktop/actualsessionend

---

# ActualSessionEnd


## [Definition](https://developer.ninjatrader.com/docs/desktop/actualsessionend#definition)


Obtains the session's end date and end time converted to the user's configured Time Zone.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


In order to obtain historical ActualSessionEnd information, you must call [GetNextSession](https://developer.ninjatrader.com/docs/desktop/getnextsession) from a stored SessionIterator object.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/actualsessionend#property-value)


A **DateTime** structure that represents end of a trading session.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/actualsessionend#syntax)


`SessionIterator.ActualSessionEnd`


## [Example](https://developer.ninjatrader.com/docs/desktop/actualsessionend#example)


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

     Print("The current session end time is " + sessionIterator.ActualSessionEnd);
   }
}
```
