# Linear Regression Slope

Source: https://developer.ninjatrader.com/docs/desktop/linear_regression_slope

---

# Linear Regression Slope


## [Description](https://developer.ninjatrader.com/docs/desktop/linear_regression_slope#description)


The Linear Regression Slope provides the slope value of the **Linear Regression** trendline.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/linear_regression_slope#syntax)


`LinRegSlope(int period)`


`LinRegSlope(ISeries<double> input, int period)`


**Returns default value**


`LinRegSlope(int period)[int barsAgo]`


`LinRegSlope(ISeries<double> input, int period)[int barsAgo]`


## [Return Value](https://developer.ninjatrader.com/docs/desktop/linear_regression_slope#return-value)


**double;** Accessing this method via an index value **[int barsAgo]** returns the indicator value of the referenced bar.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/linear_regression_slope#parameters)


| Parameter | Description |
| --- | --- |
| input | Indicator source data ([Series<`T`>](https://developer.ninjatrader.com/docs/desktop/seriest)) |
| period | Number of bars used in the calculation |


## [Examples](https://developer.ninjatrader.com/docs/desktop/linear_regression_slope#examples)


```csharp
// Prints the current slope value of a 20 period LinReg using default price type
double value = LinRegSlope(20)[0];
Print("The current slope value is " + value.ToString());

// Prints the current slope value of a 20 period LinReg using high price type
double value = LinRegSlope(High, 20)[0];
Print("The current slope value is " + value.ToString());
```


## [Source Code](https://developer.ninjatrader.com/docs/desktop/linear_regression_slope#source-code)


You can view this indicator method source code by selecting the menu New > NinjaScript Editor > Indicators within the NinjaTrader Control Center window.
