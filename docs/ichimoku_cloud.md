# Ichimoku Cloud

Source: https://developer.ninjatrader.com/docs/desktop/ichimoku_cloud

---

# Ichimoku Cloud


## [Description](https://developer.ninjatrader.com/docs/desktop/ichimoku_cloud#description)


The Ichimoku Cloud is a charting tool that shows potential support and resistance areas, trend direction, and momentum using a set of moving average-based lines and a shaded area called the ‘cloud’. It helps users observe how price interacts with these components over time.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/ichimoku_cloud#syntax)


`IchimokuCloud(int conversionPeriod, int basePeriod, int leadingSpanBPeriod, int spanDisplacement, int laggingDisplacement)`


`IchimokuCloud(ISeries<double> input, int conversionPeriod, int basePeriod, int leadingSpanBPeriod, int spanDisplacement, int laggingDisplacement)`


**Returns the Conversion value**


`IchimokuCloud(int conversionPeriod, int basePeriod, int leadingSpanBPeriod, int spanDisplacement, int laggingDisplacement).Values[0][int barsAgo]`


`IchimokuCloud(ISeries<double> input, int conversionPeriod, int basePeriod, int leadingSpanBPeriod, int spanDisplacement, int laggingDisplacement).Values[0][int barsAgo]`


**Returns the Base value**


`IchimokuCloud(int conversionPeriod, int basePeriod, int leadingSpanBPeriod, int spanDisplacement, int laggingDisplacement).Values[1][int barsAgo]`


`IchimokuCloud(ISeries<double> input, int conversionPeriod, int basePeriod, int leadingSpanBPeriod, int spanDisplacement, int laggingDisplacement).Values[1][int barsAgo]`


**Returns the LeadingSpanA value**


`IchimokuCloud(int conversionPeriod, int basePeriod, int leadingSpanBPeriod, int spanDisplacement, int laggingDisplacement).Values[2][int barsAgo]`


`IchimokuCloud(ISeries<double> input, int conversionPeriod, int basePeriod, int leadingSpanBPeriod, int spanDisplacement, int laggingDisplacement).Values[2][int barsAgo]`


**Returns the LeadingSpanB value**


`IchimokuCloud(int conversionPeriod, int basePeriod, int leadingSpanBPeriod, int spanDisplacement, int laggingDisplacement).Values[3][int barsAgo]`


`IchimokuCloud(ISeries<double> input, int conversionPeriod, int basePeriod, int leadingSpanBPeriod, int spanDisplacement, int laggingDisplacement).Values[3][int barsAgo]`


**Returns the Lagging value**


`IchimokuCloud(int conversionPeriod, int basePeriod, int leadingSpanBPeriod, int spanDisplacement, int laggingDisplacement).Values[4][int barsAgo]`


`IchimokuCloud(ISeries<double> input, int conversionPeriod, int basePeriod, int leadingSpanBPeriod, int spanDisplacement, int laggingDisplacement).Values[4][int barsAgo]`


## [Return Value](https://developer.ninjatrader.com/docs/desktop/ichimoku_cloud#return-value)


**double**; Accessing this method via an index value [int barsAgo] returns the indicator value of the referenced bar.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/ichimoku_cloud#parameters)


| input | Indicator source data ([Series<`T`>](https://developer.ninjatrader.com/docs/desktop/seriest)) |
| --- | --- |
| conversionPeriod | Conversion (Tenkan) period |
| basePeriod | Base (Kijun) period |
| leadingSpanBPeriod | Leading (Senkou) span B period |
| spanDisplacement | Span displacement |
| laggingDisplacement | Lagging (Chikou) displacement |


## [Examples](https://developer.ninjatrader.com/docs/desktop/ichimoku_cloud#examples)


```csharp
// Prints the current LeadingSpanA value
double leadingSpanAValue = IchimokuCloud(9, 26, 52, -26, 26).Values[2][0];
Print("The current Ichimoku LeadingSpanA value is " + leadingSpanAValue.ToString());
```


## [Source Code](https://developer.ninjatrader.com/docs/desktop/ichimoku_cloud#source-code)


You can view this indicator method source code by selecting the menu New > NinjaScript Editor > Indicators within the NinjaTrader Control Center window.
