# FormatPrice()

Source: https://developer.ninjatrader.com/docs/desktop/formatprice

---

# FormatPrice()


## [Definition](https://developer.ninjatrader.com/docs/desktop/formatprice#definition)


Returns a price value as a string which will be formatted to the nearest tick size.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This is useful as the standard format specifier will only use the minimum number of digits for a decimal by default; however you can use this method to ensure that your data is always formatted per the instrument tick size for easier readability. For example, a value of 1985.50 would Print() as 1985.5, while using **FormatPrice()**, we can expect the value to be formatted as 1985.50.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/formatprice#property-value)


A **string** value which will ensure the price data is always formatted to the nearest tick size.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/formatprice#syntax)


`Bars.Instrument.MasterInstrument.FormatPrice(double price, [bool round])`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/formatprice#parameters)


| --- |
| **price** | A **double** value representing a price |
| **round** | An optional bool when true (default) will round the price value to the nearest tick size |


## [Examples](https://developer.ninjatrader.com/docs/desktop/formatprice#examples)


```csharp
protected override void OnBarUpdate()
{
   // called without setting the optional bool parameter, which is defaulted to true then
   Print(Bars.Instrument.MasterInstrument.FormatPrice(Close[0]));
}

protected override void OnMarketData(MarketDataEventArgs marketDataUpdate)
{
   Print(marketDataUpdate.Instrument.MasterInstrument.FormatPrice(marketDataUpdate.Price));
```
