# Order Flow VWAP

Source: https://developer.ninjatrader.com/docs/desktop/order_flow_vwap

---

# Order Flow VWAP


## [Description](https://developer.ninjatrader.com/docs/desktop/order_flow_vwap#description)


Volume Weighted Average Price. A total of the dollars traded for every transaction (price multiplied by number of shares traded) and then divided by the total shares traded for the day. Also included are standard deviation bands.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/order_flow_vwap#syntax)


`OrderFlowVWAP(VWAPResolution resolution, TradingHours tradingHoursInstance, VWAPStandardDeviations numStandardDeviations, double sD1Multiplier, double sD2Multiplier, double sD3Multiplier)`


`OrderFlowVWAP(ISeries<double> input, VWAPResolution resolution, TradingHours tradingHoursInstance, VWAPStandardDeviations numStandardDeviations, double sD1Multiplier, double sD2Multiplier, double sD3Multiplier)`


**Returns the VWAP value**


`OrderFlowVWAP(VWAPResolution resolution, TradingHours tradingHoursInstance, VWAPStandardDeviations numStandardDeviations, double sD1Multiplier, double sD2Multiplier, double sD3Multiplier).VWAP[int barsAgo]`


`OrderFlowVWAP(ISeries<double> input, VWAPResolution resolution, TradingHours tradingHoursInstance, VWAPStandardDeviations numStandardDeviations, double sD1Multiplier, double sD2Multiplier, double sD3Multiplier).VWAP[int barsAgo]`


**Returns the StdDev1Upper value**


`OrderFlowVWAP(VWAPResolution resolution, TradingHours tradingHoursInstance, VWAPStandardDeviations numStandardDeviations, double sD1Multiplier, double sD2Multiplier, double sD3Multiplier).StdDev1Upper[int barsAgo]`


`OrderFlowVWAP(ISeries<double> input, VWAPResolution resolution, TradingHours tradingHoursInstance, VWAPStandardDeviations numStandardDeviations, double sD1Multiplier, double sD2Multiplier, double sD3Multiplier).StdDev1Upper[int barsAgo]`


**Returns the StdDev1Lower value**


`OrderFlowVWAP(VWAPResolution resolution, TradingHours tradingHoursInstance, VWAPStandardDeviations numStandardDeviations, double sD1Multiplier, double sD2Multiplier, double sD3Multiplier).StdDev1Lower[int barsAgo]`


`OrderFlowVWAP(ISeries<double> input, VWAPResolution resolution, TradingHours tradingHoursInstance, VWAPStandardDeviations numStandardDeviations, double sD1Multiplier, double sD2Multiplier, double sD3Multiplier).StdDev1Lower[int barsAgo]`


**Returns the StdDev2Upper value**


`OrderFlowVWAP(VWAPResolution resolution, TradingHours tradingHoursInstance, VWAPStandardDeviations numStandardDeviations, double sD1Multiplier, double sD2Multiplier, double sD3Multiplier).StdDev2Upper[int barsAgo]`


`OrderFlowVWAP(ISeries<double> input, VWAPResolution resolution, TradingHours tradingHoursInstance, VWAPStandardDeviations numStandardDeviations, double sD1Multiplier, double sD2Multiplier, double sD3Multiplier).StdDev2Upper[int barsAgo]`


**Returns the StdDev2Lower value**


`OrderFlowVWAP(VWAPResolution resolution, TradingHours tradingHoursInstance, VWAPStandardDeviations numStandardDeviations, double sD1Multiplier, double sD2Multiplier, double sD3Multiplier).StdDev2Lower[int barsAgo]`


`OrderFlowVWAP(ISeries<double> input, VWAPResolution resolution, TradingHours tradingHoursInstance, VWAPStandardDeviations numStandardDeviations, double sD1Multiplier, double sD2Multiplier, double sD3Multiplier).StdDev2Lower[int barsAgo]`


**Returns the StdDev3Upper value**


`OrderFlowVWAP(VWAPResolution resolution, TradingHours tradingHoursInstance, VWAPStandardDeviations numStandardDeviations, double sD1Multiplier, double sD2Multiplier, double sD3Multiplier).StdDev3Upper[int barsAgo]`


`OrderFlowVWAP(ISeries<double> input, VWAPResolution resolution, TradingHours tradingHoursInstance, VWAPStandardDeviations numStandardDeviations, double sD1Multiplier, double sD2Multiplier, double sD3Multiplier).StdDev3Upper[int barsAgo]`


**Returns the StdDev3Lower value**


`OrderFlowVWAP(VWAPResolution resolution, TradingHours tradingHoursInstance, VWAPStandardDeviations numStandardDeviations, double sD1Multiplier, double sD2Multiplier, double sD3Multiplier).StdDev3Lower[int barsAgo]`


`OrderFlowVWAP(ISeries<double> input, VWAPResolution resolution, TradingHours tradingHoursInstance, VWAPStandardDeviations numStandardDeviations, double sD1Multiplier, double sD2Multiplier, double sD3Multiplier).StdDev3Lower[int barsAgo]`


## [Return Value](https://developer.ninjatrader.com/docs/desktop/order_flow_vwap#return-value)


**double;** Accessing this method via an index value [int barsAgo] returns the indicator value of the referenced bar.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/order_flow_vwap#parameters)


| input | Indicator source data ([Series<`T`>](https://developer.ninjatrader.com/docs/desktop/seriest)) |
| --- | --- |
| resolution | The data the indicator will run off of: Standard, Tick |
| tradingHoursInstance | The trading hour template that will indicate when the VWAP resets |
| numStandardDeviations | The number of standard deviations of the VWAP |
| sD1Multiplier | The multiplier for the first standard deviation |
| sD2Multiplier | The multiplier for the second standard deviation |
| sD3Multiplier | The multiplier for the third standard deviation |


## [Examples](https://developer.ninjatrader.com/docs/desktop/order_flow_vwap#examples)


```csharp
// A 1 tick data series must be added to the OnStateChange() if using a Tick Resolution (our second example call below in OnBarUpdate())
else if (State == State.Configure)
{
  AddDataSeries(Data.BarsPeriodType.Tick, 1);
}

// OnBarUpdate() logic
if (BarsInProgress == 0)
{
  // Prints the VWAP value using a standard resolution off of RTH trading hours
  double VWAPValue = OrderFlowVWAP(VWAPResolution.Standard, TradingHours.String2TradingHours("CME US Index Futures RTH"), VWAPStandardDeviations.Three, 1, 2, 3).VWAP[0];
  Print("The current VWAP with a standard resolution on CME US Index Futures RTH is " + VWAPValue.ToString());

// Prints the first upper standard deviation value using a tick resolution off of trading hours of the Data Series
  double VWAPStdDevUp1 = OrderFlowVWAP(VWAPResolution.Tick, Bars.TradingHours, VWAPStandardDeviations.Three, 1, 2, 3).StdDev1Upper[0];
  Print("The current VWAP with a tick resolution on " + Bars.TradingHours.ToString() + " is " + VWAPStdDevUp1.ToString());
}
else if (BarsInProgress == 1)
{
  // We have to update the secondary tick series of the cached indicator using Tick Resolution to make sure the values we get in BarsInProgress == 0 are in sync
  OrderFlowVWAP(BarsArray[0], VWAPResolution.Tick, BarsArray[0].TradingHours, VWAPStandardDeviations.Three, 1, 2, 3).Update(OrderFlowVWAP(BarsArray[0], VWAPResolution.Tick, BarsArray[0].TradingHours, VWAPStandardDeviations.Three, 1, 2, 3).BarsArray[1].Count - 1, 1);
}
```

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


- Referencing multiple **OrderFlowVWAP**'s with different ResetInterval’s in a single NinjaScript Indicator / Strategy is not supported by default. Please contact [platformsupport@ninjatrader.com](mailto:platformsupport@ninjatrader.com) for a workaround.
- Referencing **OrderFlowVWAP** in a NinjaScript indicator or strategy which runs on either **Calcuate.OnEachTick** or **.OnPriceChange**, historical data is needed for accurate calculations.
