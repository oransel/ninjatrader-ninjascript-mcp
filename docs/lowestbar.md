# LowestBar()

Source: https://developer.ninjatrader.com/docs/desktop/lowestbar

---

# LowestBar()


## [Definition](https://developer.ninjatrader.com/docs/desktop/lowestbar#definition)


Returns the number of bars ago the lowest price value occurred within the specified look-back period.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/lowestbar#method-return-value)


An **int** value representing a value of bars ago.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/lowestbar#syntax)


`LowestBar(ISeries<double> series, int period)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/lowestbar#parameters)


| --- |
| **period** | The number of bars to check for the test condition |
| **series** | Any **Series<`double`>** type object such as an indicator, **Close**, **High**, **Low**, etc... |


## [Examples](https://developer.ninjatrader.com/docs/desktop/lowestbar#examples)


```csharp
protected override void OnBarUpdate()
{
   // store the lowest bar ago value
   int lowestBar = LowestBar(Low, Bars.BarsSinceNewTradingDay);

   //evaluate low price from lowest bar ago value
   double lowestPrice = Low[lowestBar];

   //Printed result:  Lowest price of the session: 2087.25 - occurred 362 bars ago
   Print(string.Format("Lowest price of the session: {0} - occurred {1} bars ago", lowestPrice, lowestBar));
}
```
