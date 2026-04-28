# SessionIterator

Source: https://developer.ninjatrader.com/docs/desktop/sessioniterator

---

# SessionIterator


## [Definition](https://developer.ninjatrader.com/docs/desktop/sessioniterator#definition)


Allows you to traverse through various trading hours data elements which apply to a segment of bars.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Should you wish to obtain trading hours information for historical bar values, you need to construct and store your own session iterator object based of the desired bars series array.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/sessioniterator#parameters)


| bars | The **Bars** object used to create the SessionIterator |
| --- | --- |

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


Warning: The properties in this class should NOT be accessed within the **OnStateChange()** method before the State has reached State.DataLoaded.


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/sessioniterator#methods-and-properties)


| Method/Property | Description |
| --- | --- |
| [ActualSessionBegin](https://developer.ninjatrader.com/docs/desktop/actualsessionbegin) | Obtains the sessions start day and start time converted to the PC's local time zone |
| [ActualSessionEnd](https://developer.ninjatrader.com/docs/desktop/actualsessionend) | Obtains the sessions end day and end time converted to the PC's local time zone |
| [ActualTradingDayEndLocal](https://developer.ninjatrader.com/docs/desktop/actualtradingdayendlocal) | Returns the sessions End-Of-Day (EOD) in the local timezone |
| [ActualTradingDayExchange](https://developer.ninjatrader.com/docs/desktop/actualtradingdayexchange) | Obtains the date of a session representing the trading date of the exchange |
| [CalculateTradingDay()](https://developer.ninjatrader.com/docs/desktop/calculatetradingday) | Calculates the current trading date of a specified date |
| [GetNextSession()](https://developer.ninjatrader.com/docs/desktop/getnextsession) | Calculates the next available session relative to a specified date |
| [GetTradingDay()](https://developer.ninjatrader.com/docs/desktop/gettradingday) | Returns the actual trading date based on the exchange |
| [GetTradingDayBeginLocal()](https://developer.ninjatrader.com/docs/desktop/gettradingdaybeginlocal) | Converts the trading day begin time from the exchange timezone to local time |
| [GetTradingDayEndLocal()](https://developer.ninjatrader.com/docs/desktop/gettradingdayendlocal) | Converts the trading day end time from the exchange timezone to local time |
| [IsInSession()](https://developer.ninjatrader.com/docs/desktop/isinsession) | Indicates if a specified date is within the bounds of the current session |
| [IsNewSession()](https://developer.ninjatrader.com/docs/desktop/isnewsession) | Indicates if a specified time is greater than the actual session end of the current session |
| [IsTradingDayDefined()](https://developer.ninjatrader.com/docs/desktop/istradingdaydefined) | Indicates if a trading day is defined for a specific date |

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Tip: In order to calculate a session information for another multi-instrument or multi-time frame script, you can pass in the desired **BarsArray** array value as the SessionIterator bars object.


## [Examples](https://developer.ninjatrader.com/docs/desktop/sessioniterator#examples)


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
    // on new bars session, find the next trading session
    if (Bars.IsFirstBarOfSession)
    {
        Print("Calculating trading day for " + Time[0]);
        // use the current bar time to calculate the next session
        sessionIterator.GetNextSession(Time[0], true);

        // store the desired session information
        DateTime tradingDay   = sessionIterator.ActualTradingDayExchange;
        DateTime beginTime    = sessionIterator.ActualSessionBegin;
        DateTime endTime      = sessionIterator.ActualSessionEnd;

        Print(string.Format("The Current Trading Day {0} starts at {1} and ends at {2}",
                            tradingDay.ToShortDateString(), beginTime, endTime));
        // Output:
        // Calculating trading day from 9/30/2015 4:01:00 PM
        //The Current Trading Day 10/1/2015 starts at 9/30/2015 4:00:00 PM and ends at 10/1/2015 3:00:00 PM
    }
}
```
