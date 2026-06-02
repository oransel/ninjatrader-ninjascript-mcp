# Money Flow Oscillator

Source: https://developer.ninjatrader.com/docs/desktop/money_flow_oscillator

---

# Money Flow Oscillator


## [Description](https://developer.ninjatrader.com/docs/desktop/money_flow_oscillator#description)


The Money Flow Oscillator measures the amount of money flow volume over a specific period. A move into positive territory indicates buying pressure while a move into negative territory indicates selling pressure.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/money_flow_oscillator#syntax)


`MoneyFlowOscillator(int period)`


`MoneyFlowOscillator(ISeries<double> input, int period)`


## [Return Value](https://developer.ninjatrader.com/docs/desktop/money_flow_oscillator#return-value)


**double;** Accessing this method via an index value `[int barsAgo]` returns the indicator value of the referenced bar.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/money_flow_oscillator#parameters)


| Parameter | Description |
| --- | --- |
| input | Indicator source data ([Series<`T`>](https://developer.ninjatrader.com/docs/desktop/seriest)) |
| period | Number of bars used in the calculation |


## [Examples](https://developer.ninjatrader.com/docs/desktop/money_flow_oscillator#examples)


```csharp
// Prints the current value of a 10 period Money Flow Oscillator
double value = MoneyFlowOscillator(10)[0];
Print("The current Money Flow Oscillator value is " + value.ToString());
```
