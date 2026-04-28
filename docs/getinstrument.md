# GetInstrument()

Source: https://developer.ninjatrader.com/docs/desktop/getinstrument

---

# GetInstrument()


## [Definition](https://developer.ninjatrader.com/docs/desktop/getinstrument#definition)


Returns an **Instrument** object by the master instrument name configured in the database.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This method does NOT add additional data for real-time or historical processing. For adding additional data to your script, please see the **AddDataSeries()** method.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/getinstrument#method-return-value)


An **Instrument** object


## [Syntax](https://developer.ninjatrader.com/docs/desktop/getinstrument#syntax)


`Instrument.GetInstrument(string instrumentName)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/getinstrument#parameters)


| --- |
| **instrumentName** | A **string** value representing a name of an instrument |


## [Examples](https://developer.ninjatrader.com/docs/desktop/getinstrument#examples)


```csharp
protected override void OnStateChange()
{
    if (State == State.Historical)
    {
        Instrument myInstrument = Instrument.GetInstrument("AAPL");

        Print("AAPL's tick size is " + myInstrument.MasterInstrument.TickSize.ToString());
    }
}
```
