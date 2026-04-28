# Volumes

Source: https://developer.ninjatrader.com/docs/desktop/volumes

---

# Volumes


## [Definition](https://developer.ninjatrader.com/docs/desktop/volumes#definition)


Holds an array of **ISeries`<double>`** objects holding historical bar volumes. An **ISeries`<double>`** object is added to this array when calling the [AddDataSeries()](https://developer.ninjatrader.com/docs/desktop/adddataseries) method. Its purpose is to provide access to the volumes of all Bars objects in a multi-instrument or multi-time frame script.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


For working with [Cryptocurrency instruments](https://developer.ninjatrader.com/docs/desktop/instrumenttype) which report volume fractional, please use the [VOL()](https://developer.ninjatrader.com/docs/desktop/volume) indicator series, or store the volume for your script in a custom variable and convert alongside our [VOL()](https://developer.ninjatrader.com/docs/desktop/volume) indicator `Instrument.MasterInstrument.InstrumentType == InstrumentType.CryptoCurrency ? Core.Globals.ToCryptocurrencyVolume((long)Volume[0]) : Volume[0]`).


## [Property Value](https://developer.ninjatrader.com/docs/desktop/volumes#property-value)


An array of **ISeries`<double>`** objects.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/volumes#syntax)


`Volumes[int barSeriesIndex][int barsAgo]`


## [Examples](https://developer.ninjatrader.com/docs/desktop/volumes#examples)


```csharp
protected override void OnStateChange()
{
     if (State == State.Configure)
     {
         // Adds a 5-minute Bars object to the strategy and is automatically assigned
         // a Bars object index of 1 since the primary data the strategy is run against
         // set by the UI takes the index of 0.
         AddDataSeries("AAPL", BarsPeriodType.Minute, 5);
     }
}

protected override void OnBarUpdate()
{
     // Compares the primary bar's volume to the 5-minute bar's volume
     if (Volumes[0][0] > Volumes[1][0])
         Print("The primary bar's volume is greater");
}
```
