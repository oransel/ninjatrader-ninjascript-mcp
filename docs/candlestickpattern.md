# CandleStickPattern

Source: https://developer.ninjatrader.com/docs/desktop/candlestickpattern

---

# CandleStickPattern


## [Description](https://developer.ninjatrader.com/docs/desktop/candlestickpattern#description)


Detects the specified candle stick pattern.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/candlestickpattern#syntax)


`CandleStickPattern(ChartPattern pattern, int trendStrength)`


`CandleStickPattern(ISeries<double> input, ChartPattern pattern, int trendStrength)`


**Returns a value indicating if the specified pattern was detected**


`CandleStickPattern(ChartPattern pattern, int trendStrength)[int barsAgo]`


`CandleStickPattern(ISeries<double> input, ChartPattern pattern, int trendStrength)[int barsAgo]`


## [Return Value](https://developer.ninjatrader.com/docs/desktop/candlestickpattern#return-value)


A **double** value representing pattern found. Returns a value of 1 if the pattern is found; returns a value of 0 if no pattern was found.


Accessing this method via an index value `[int barsAgo]` returns the indicator value of the referenced bar.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/candlestickpattern#parameters)


| --- |
| input | Indicator source data ([Series<`T`>](https://developer.ninjatrader.com/docs/desktop/seriest)) |
| pattern | Possible values are:

- **ChartPattern.BearishBeltHold**
- **ChartPattern.BearishEngulfing**
- **ChartPattern.BearishHarami**
- **ChartPattern.BearishHaramiCross**
- **ChartPattern.BullishBeltHold**
- **ChartPattern.BullishEngulfing**
- **ChartPattern.BullishHarami**
- **ChartPattern.BullishHaramiCross**
- **ChartPattern.DarkCloudCover**
- **ChartPattern.Doji**
- **ChartPattern.DownsideTasukiGap**
- **ChartPattern.EveningStar**
- **ChartPattern.FallingThreeMethods**
- **ChartPattern.Hammer**
- **ChartPattern.HangingMan**
- **ChartPattern.InvertedHammer**
- **ChartPattern.MorningStart**
- **ChartPattern.PiercingLine**
- **ChartPattern.RisingThreeMethods**
- **ChartPattern.ShootingStar**
- **ChartPattern.StickSandwich**
- **ChartPattern.ThreeBlackCrows**
- **ChartPattern.ThreeWhiteSoldiers**
- **ChartPattern.UpsideGapTwoCrows**
- **ChartPattern.UpsideTasukiGap** |
| trendStrength | The number of required bars to the left and right of the swing point used to determine trend. A value of zero will exclude the requirement of a trend and only detect based on the candles themselves. |


## [Examples](https://developer.ninjatrader.com/docs/desktop/candlestickpattern#examples)


```csharp
// Go long if the current bar is a bullish engulfing pattern
if (CandleStickPattern(ChartPattern.BullishEngulfing, 4)[0] == 1)
    EnterLong();
```


## [Source Code](https://developer.ninjatrader.com/docs/desktop/candlestickpattern#source-code)


You can view this indicator method source code by selecting the menu New > NinjaScript Editor > Indicators within the NinjaTrader Control Center window.
