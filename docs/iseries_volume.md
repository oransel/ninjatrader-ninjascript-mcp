# Volume

Source: https://developer.ninjatrader.com/docs/desktop/iseries_volume

---

# Volume


## [Definition](https://developer.ninjatrader.com/docs/desktop/iseries_volume#definition)


A collection of historical bar volume values.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


For working with **Cryptocurrency instruments** which report volume fractional, please use the **VOL()** indicator series, or store the volume for your script in a custom variable and convert alongside our **VOL()** indicator (`Instrument.MasterInstrument.InstrumentType == InstrumentType.CryptoCurrency ? Core.Globals.ToCryptocurrencyVolume((long)Volume[0]) : Volume[0]`).


## [Property Value](https://developer.ninjatrader.com/docs/desktop/iseries_volume#property-value)


An **ISeries`<double>`** object. Accessing this property via an index `[int barsAgo]` returns A **double** value representing the volume of the referenced bar.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/iseries_volume#syntax)


`Volume`


`Volume[int barsAgo]`


## [Examples](https://developer.ninjatrader.com/docs/desktop/iseries_volume#examples)


```csharp
// OnBarUpdate method**
protected override void OnBarUpdate()
{
     // Is current volume greater than twice the prior bar's volume
     if (Volume[0] > Volume[1] * 2)
         Print("We have increased volume");

     // Is the current volume greater than the 20 period moving average of volume

     if (Volume[0] > SMA(Volume, 20)[0])

         Print("Increasing volume");
}
```
