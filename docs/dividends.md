# Dividends

Source: https://developer.ninjatrader.com/docs/desktop/dividends

---

# Dividends


## [Definition](https://developer.ninjatrader.com/docs/desktop/dividends#definition)


An collection of Dividends configured for the **Master Instrument properties** used in for stocks.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/dividends#property-value)


A collection of Dividends configured for the current instrument.


Possible values are:


| Amount | Date |
| --- | --- |
| A **double** value representing the amount in dollars which was paid on the date of the dividend | A DateTime structure representing the date of the dividend |


## [Syntax](https://developer.ninjatrader.com/docs/desktop/dividends#syntax)


`Bars.Instrument.MasterInstrument.Dividends`


## [Examples](https://developer.ninjatrader.com/docs/desktop/dividends#examples)


```csharp
foreach(Dividend dividends in Bars.Instrument.MasterInstrument.Dividends)
{
   Print(dividends.Amount);
   Print(dividends.Date);
}
```
