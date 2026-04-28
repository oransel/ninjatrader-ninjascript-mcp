# Choppiness Index

Source: https://developer.ninjatrader.com/docs/desktop/choppiness_index

---

# Choppiness Index


## [Description](https://developer.ninjatrader.com/docs/desktop/choppiness_index#description)


The Choppiness Index is designed to determine if the market is choppy (trading sideways) or not choppy (trading within a trend in either direction).


## [Syntax](https://developer.ninjatrader.com/docs/desktop/choppiness_index#syntax)


`ChoppinessIndex(int period)`


`ChoppinessIndex(ISeries<double> input, int period)`


## [Return Value](https://developer.ninjatrader.com/docs/desktop/choppiness_index#return-value)


**double;** Accessing this method via an index value **int barsAgo** returns the indicator value of the referenced bar.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/choppiness_index#parameters)


| --- |
| **input** | Indicator source data ([Series<`T`>](https://developer.ninjatrader.com/docs/desktop/seriest)) |
| **period** | Number of bars used in the calculation |


## [Examples](https://developer.ninjatrader.com/docs/desktop/choppiness_index#examples)


```csharp
// Prints the current value of a 14 period Choppiness Index
double value = ChoppinessIndex(14)[0];
Print("The current Choppiness Index value is " + value.ToString());
```
