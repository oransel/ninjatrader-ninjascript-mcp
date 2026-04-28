# Splits

Source: https://developer.ninjatrader.com/docs/desktop/splits

---

# Splits


## [Definition](https://developer.ninjatrader.com/docs/desktop/splits#definition)


Indicates the Splits that have been configured for the **Master Instrument properties** used in for stocks.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/splits#property-value)


A collection of Splits configured for the current instrument.


Possible values are:


| Date | Factor |
| --- | --- |
| A DateTime structure representing the date of the split | A **double** value representing the number of points the stock split |


## [Syntax](https://developer.ninjatrader.com/docs/desktop/splits#syntax)


`Bars.Instrument.MasterInstrument.Splits`


## [Examples](https://developer.ninjatrader.com/docs/desktop/splits#examples)


```csharp
foreach (Split split in Bars.Instrument.MasterInstrument.Splits)
{
     Print(split.Date);
     Print(split.Factor);
}
```
