# McClellan Oscillator

Source: https://developer.ninjatrader.com/docs/desktop/mcclellan_oscillator

---

# McClellan Oscillator


## [Description](https://developer.ninjatrader.com/docs/desktop/mcclellan_oscillator#description)


McClellan Oscillator is the difference between two exponential moving averages of the NYSE advance decline spread. This indicator requires ADV and DECL index data.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/mcclellan_oscillator#syntax)


`McClellanOscillator(int fastPeriod, int slowPeriod)`


`McClellanOscillator(ISeries<double> input, int fastPeriod, int slowPeriod)`


## [Return Value](https://developer.ninjatrader.com/docs/desktop/mcclellan_oscillator#return-value)


**double**; Accessing this method via an index value **int barsAgo** returns the indicator value of the referenced bar.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/mcclellan_oscillator#parameters)


| --- |
| **input** | Indicator source data ([Series<`T`>](https://developer.ninjatrader.com/docs/desktop/seriest)) |
| **fastPeriod** | Number of bars used in the fast moving average calculation |
| **slowPeriod** | Number of bars used in the slow moving average calculation |


## [Examples](https://developer.ninjatrader.com/docs/desktop/mcclellan_oscillator#examples)


```csharp
// An ADV and DECL data series must be added to OnStateChange()
else if (State == State.Configure)
{
    AddDataSeries("^ADV");
    AddDataSeries("^DECL");
}

// Prints the current value of the McClellan Oscillator with a 19 fast period moving average & 39 slow period
double value = McClellanOscillator(19, 39)[0];
Print("The current McClellan Oscillator value is " + value.ToString());
```
