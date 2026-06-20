# Valid Input Data for Indicator Methods

Source: https://developer.ninjatrader.com/docs/desktop/valid_input_data_for_indicator

---

# Valid Input Data for Indicator Methods


System indicator methods require valid input data to function property. Indicator methods can accept the following forms of input data:


## [Default Input](https://developer.ninjatrader.com/docs/desktop/valid_input_data_for_indicator#default-input)


The default input (Inputs[[BarsInProgress](https://developer.ninjatrader.com/docs/desktop/barsinprogress)) of the custom indicator, Market Analyzer row or strategy is used if input is not specified.


```csharp
// Printing the current value of the 10 period SMA of closing prices
// using the default input.
double value = SMA(10)[0];
Print("The current SMA value is " + value.ToString());
```


## [Price Series](https://developer.ninjatrader.com/docs/desktop/valid_input_data_for_indicator#price-series)


Open, High, Low, Close and Volume can all be used as input for an indicator method.


```csharp
// Passing in the a price series of High prices and printing out the current value of the
// 14 period simple moving average
double value = SMA(High, 14)[0];
Print("The current SMA value is " + value.ToString());
```


## [Indicator](https://developer.ninjatrader.com/docs/desktop/valid_input_data_for_indicator#indicator)


Indicators can be used as input for other indicators.


```csharp
// Printing the current value of the 20 period simple moving average of a 14 period RSI
// using a data series of closing prices
double value = SMA(RSI(Close, 14, 3), 20)[0];
Print("The current SMA value is " + value.ToString());
```


## [Series<`double`>](https://developer.ninjatrader.com/docs/desktop/valid_input_data_for_indicator#series%3C-%3E)


[Series<`double`>](https://developer.ninjatrader.com/docs/desktop/seriest) can be used as input for indicators.


```csharp
// Instantiating a new Series<double> object and passing it in as input to calculate
// a simple moving average
Series<double> myDataSeries = new Series<double>(this);
double value = SMA(myDataSeries, 20)[0];
```


## [Bars Object](https://developer.ninjatrader.com/docs/desktop/valid_input_data_for_indicator#bars-object)


A Bars object (which holds a series that contains OHLC data) can be used as input for indicators.


```csharp
// Passing in the second Bars object held in a multi-instrument and timeframe strategy
// The default value used for the SMA calculation is the close price
double value = SMA(BarsArray[1], 20)[0];
Print("The current SMA value is " + value.ToString());;
```

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Tip: The input series of an indicator cannot be the hosting indicator itself, as this will cause recursive loops.


```csharp
// Using the hosting indicator in this way will cause errors with recursive loops
double value = SMA(this, 20)[0];|
```
