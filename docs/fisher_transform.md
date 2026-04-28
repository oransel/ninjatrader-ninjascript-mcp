# Fisher Transform

Source: https://developer.ninjatrader.com/docs/desktop/fisher_transform

---

# Fisher Transform


## [Description](https://developer.ninjatrader.com/docs/desktop/fisher_transform#description)


With distinct turning points and a rapid response time, the Fisher Transform uses the assumption that while prices do not have a normal or Gaussian probability density function (that familiar bell-shaped curve), you can create a nearly Gaussian probability density function by normalizing price (or an indicator such as **RSI**) and applying the Fisher Transform. Use the resulting peak swings to clearly identify price reversals.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/fisher_transform#syntax)


`FisherTransform(int period)`


`FisherTransform(ISeries<double> input, int period)`


**Returns default value**


`FisherTransform(int period)[int barsAgo]`


`FisherTransform(ISeries<double> input, int period)[int barsAgo]`


## [Return Value](https://developer.ninjatrader.com/docs/desktop/fisher_transform#return-value)


**double;** Accessing this method via an index value `[int barsAgo]` returns the indicator value of the referenced bar.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/fisher_transform#parameters)


| --- |
| input | Indicator source data ([Series<`T`>](https://developer.ninjatrader.com/docs/desktop/seriest)) |
| period | Number of bars used in the calculation |


## [Examples](https://developer.ninjatrader.com/docs/desktop/fisher_transform#examples)


```csharp
// Prints the current value of a 10 period using default (median) price type
double value = FisherTransform(10)[0];
Print("The current Fisher Transform value is " + value.ToString());
```


## [Source Code](https://developer.ninjatrader.com/docs/desktop/fisher_transform#source-code)


You can view this indicator method source code by selecting the menu New > NinjaScript Editor > Indicators within the NinjaTrader Control Center window.
