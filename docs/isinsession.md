# IsInSession()

Source: https://developer.ninjatrader.com/docs/desktop/isinsession

---

# IsInSession()


## [Definition](https://developer.ninjatrader.com/docs/desktop/isinsession#definition)


Indicates a specified date is within the bounds of the current session, according to the configured Trading Hours template.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Additionally this method will internally trigger a **GetNextSession()** call to calculate the next available session relative to the "timeLocal" value used in the method's input.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/isinsession#property-value)


A **bool** value when true indicates the specified time is within the current trading session; otherwise false.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/isinsession#parameters)


| --- |
| **timeLocal** | The DateTime value used to calculate the next trading day. |
| **includesEndTimeStamp** | A bool determining if a timestamp of <`n`>:00 should fall into the current session. (e.g., used for time based intraday series such as minute or second). |
| **isIntraDay** | A bool determining if **IsInSession()** considers the time of day (when true) or only the date (when false). |


## [Syntax](https://developer.ninjatrader.com/docs/desktop/isinsession#syntax)


`<sessioniterator>.IsInSession(DateTime timeLocal, bool includesEndTimeStamp, bool isIntraDay)`


## [Examples](https://developer.ninjatrader.com/docs/desktop/isinsession#examples)


```csharp
private SessionIterator sessionIterator;

protected override void OnStateChange()
{
    if (State == State.Historical)
    {
        //stores the sessions once bars are ready, but before OnBarUpdate is called
        sessionIterator = new SessionIterator(Bars);
    }
}

protected override void OnBarUpdate()
{
    // Only place an order if the time three hours from now will still be within the current session
    if (sessionIterator.IsInSession(DateTime.Now.AddHours(3), true, true) /* && additional conditions here */)
        EnterLongStopMarket(CurrentDayOHL().High[0] + TickSize);
}
```
