# Balance of Power (BOP)

Source: https://developer.ninjatrader.com/docs/desktop/balance_of_power_bop

---

# Balance of Power (BOP)


## [Description](https://developer.ninjatrader.com/docs/desktop/balance_of_power_bop#description)


The balance of power (BOP) indicator measures the strength of the bulls vs. bears by assessing the ability of each to push price to an extreme level.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/balance_of_power_bop#syntax)


`BOP(int smooth)`


`BOP(ISeries<double> input, int smooth)`


**Returns default value**


`BOP(int smooth)[int barsAgo]`


`BOP(ISeries<double> input, int smooth)[int barsAgo]`


## [Return Value](https://developer.ninjatrader.com/docs/desktop/balance_of_power_bop#return-value)


**double**; Accessing this method via an index value `[int barsAgo]` returns the indicator value of the referenced bar.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/balance_of_power_bop#parameters)


| --- |
| input | Indicator source data |
| smooth | The smoothing period |


## [Example](https://developer.ninjatrader.com/docs/desktop/balance_of_power_bop#example)


```csharp
// Prints the current value of BOP using default price type and 3 period smoothing
double value = BOP(3)[0];
Print("The current BOP value is " + value.ToString());
```


## [Source Code](https://developer.ninjatrader.com/docs/desktop/balance_of_power_bop#source-code)


You can view this indicator method source code by selecting the menu New > NinjaScript Editor > Indicators within the NinjaTrader Control Center window.
