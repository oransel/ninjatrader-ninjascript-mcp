# Relative Vigor Index

Source: https://developer.ninjatrader.com/docs/desktop/relative_vigor_index

---

# Relative Vigor Index


## [Description](https://developer.ninjatrader.com/docs/desktop/relative_vigor_index#description)


The Relative Vigor Index measures the strength of a trend by comparing an instruments closing price to its price range. It's based on the fact that prices tend to close higher than they open in up trends, and closer lower than they open in downtrends.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/relative_vigor_index#syntax)


`RelativeVigorIndex(int period)`


`RelativeVigorIndex(ISeries<double> input, int period)`


## [Return Value](https://developer.ninjatrader.com/docs/desktop/relative_vigor_index#return-value)


**double;** Accessing this method via an index value `[int barsAgo]` returns the indicator value of the referenced bar.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/relative_vigor_index#parameters)


| Parameter | Description |
| --- | --- |
| input | Indicator source data ([Series<`T`>](https://developer.ninjatrader.com/docs/desktop/seriest)) |
| period | Number of bars used in the calculation |


## [Examples](https://developer.ninjatrader.com/docs/desktop/relative_vigor_index#examples)


```csharp
// Prints the current value of a 10 period Relative Vigor Index
double value = RelativeVigorIndex(10)[0];
Print("The current Relative Vigor Index value is " + value.ToString());
```
