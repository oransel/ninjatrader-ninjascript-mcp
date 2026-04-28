# Stochastics RSI (StochRSI)

Source: https://developer.ninjatrader.com/docs/desktop/stochastics_rsi_stochrsi

---

# Stochastics RSI (StochRSI)


## [Description](https://developer.ninjatrader.com/docs/desktop/stochastics_rsi_stochrsi#description)


This is an indicator on indicator implementation. It is simply a **[Stochastics](https://developer.ninjatrader.com/docs/desktop/stochastics)** indicator applied on **[RSI](https://developer.ninjatrader.com/docs/desktop/relative_strength_index_rsi)**.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/stochastics_rsi_stochrsi#syntax)


`StochRSI(int period)`


`StochRSI(ISeries<double> input, int period)`


**Returns default value**


`StochRSI(int period)[int barsAgo]`


`StochRSI[ISeries<double> input, int period)[int barsAgo]`


## [Return Value](https://developer.ninjatrader.com/docs/desktop/stochastics_rsi_stochrsi#return-value)


**double;** Accessing this method via an index value `[int barsAgo]` returns the indicator value of the referenced bar.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/stochastics_rsi_stochrsi#parameters)


| Parameter | Description |
| --- | --- |
| input | Indicator source data ([Series<`T`>](https://developer.ninjatrader.com/docs/desktop/seriest)) |
| period | Number of bars used in the calculation |


## [Examples](https://developer.ninjatrader.com/docs/desktop/stochastics_rsi_stochrsi#examples)


```csharp
// Evaluates if the current bar StochRSI value is greater than the value one bar ago
if (StochRSI(14)[0] > StochRSI(14)[1])
   Print("Stochastics RSI is rising");
```


## [Source Code](https://developer.ninjatrader.com/docs/desktop/stochastics_rsi_stochrsi#source-code)


You can view this indicator method source code by selecting the menu New > NinjaScript Editor > Indicators within the NinjaTrader Control Center window.
