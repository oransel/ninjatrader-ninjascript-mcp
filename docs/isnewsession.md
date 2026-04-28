# IsNewSession()

Source: https://developer.ninjatrader.com/docs/desktop/isnewsession

---

# IsNewSession()


## [Definition](https://developer.ninjatrader.com/docs/desktop/isnewsession#definition)


Indicates a specified time is greater than the **ActualSessionEnd** property on the configured Trading Hours template.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/isnewsession#property-value)


A bool value when true indicates the specified time is later than **ActualSessionEnd**; otherwise false.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/isnewsession#parameters)


| --- |
| **time** | The DateTime value used to compare |
| **includesEndTimeStamp** | A bool determining if a timestamp of <`n`>:00 should fall into the current session. (e.g., used for time based intraday series such as minute or second). |


## [Syntax](https://developer.ninjatrader.com/docs/desktop/isnewsession#syntax)


`<sessioniterator>.IsNewSession(DateTime time, bool includesEndTimeStamp)`


## [Examples](https://developer.ninjatrader.com/docs/desktop/isnewsession#examples)


```csharp
bool takeTrades;

protected override void OnBarUpdate()
{
    // Switch a bool named takeTrades to false when IsNewSession() returns true.
    if (Bars.SessionIterator.IsNewSession(DateTime.Now, true)) ;
    {
        Alert("EOS", Priority.Medium, String.Format("New session beginning. Waiting until {0} to begin trading again"), " ", 5, Brushes.Black, Brushes.White);
        takeTrades = false;
    }

    // Set the bool back to true on the first bar of the new session
    if (Bars.IsFirstBarOfSession)
        takeTrades = true;
}
```
