# AddHeikenAshi()

Source: https://developer.ninjatrader.com/docs/desktop/addheikenashi

---

# AddHeikenAshi()


## [Definition](https://developer.ninjatrader.com/docs/desktop/addheikenashi#definition)


Similar to the [AddDataSeries()](https://developer.ninjatrader.com/docs/desktop/adddataseries) method for adding Bars objects, this method adds a Heiken Ashi Bars object for multi-series NinjaScript.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


- When running NinjaScript, you will be able to choose the first instrument and bar interval to run on. This first Bars object will carry a [BarsInProgress](https://developer.ninjatrader.com/docs/desktop/barsinprogress) index of 0.
- In a multi-time frame and multi-instrument NinjaScript, supplementary Bars objects are added via this method in State.Configure state of the [OnStateChange()](https://developer.ninjatrader.com/docs/desktop/onstatechange) method and given an incremented BarsInProgress index value. See additional information on running [multi-bars scripts](https://developer.ninjatrader.com/docs/desktop/multi_time_frame_instruments).
- The [BarsInProgress](https://developer.ninjatrader.com/docs/desktop/barsinprogress) property can be used to filter updates between different bars series
- If using [OnMarketData()](https://developer.ninjatrader.com/docs/desktop/onmarketdata), a subscription will be created on all bars series added in your indicator or strategy strategy (even if the instrument is the same). The market data subscription behavior occurs both in real-time and during [TickReplay](https://developer.ninjatrader.com/docs/desktop/developing_for_tick_replay) historical
- For adding regular Bars types please use [AddDataSeries()](https://developer.ninjatrader.com/docs/desktop/adddataseries)
- A Tick Replay indicator or strategy CANNOT use a MarketDataType.Ask or MarketDataType.Bid series. Please see [Developing for Tick Replay](https://developer.ninjatrader.com/docs/desktop/developing_for_tick_replay) for more information.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/addheikenashi#syntax)


`AddHeikenAshi(string instrumentName, Data.BarsPeriodType baseBarsPeriodType, int baseBarsPeriodTypeValue, Data.MarketDataType marketDataType)`


`AddHeikenAshi(string instrumentName, Data.BarsPeriodType baseBarsPeriodType, int baseBarsPeriodTypeValue, Data.MarketDataType marketDataType, string tradingHoursName)`


`AddHeikenAshi(string instrumentName, Data.BarsPeriodType baseBarsPeriodType, int baseBarsPeriodTypeValue, Data.MarketDataType marketDataType, string tradingHoursName, bool? isResetOnNewTradingDay)`
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


- This method should ONLY be called from the [OnStateChange()](https://developer.ninjatrader.com/docs/desktop/onstatechange) method during State.Configure
- Should your script be the host for other scripts that are creating indicators and series dependent resources in State.DataLoaded, please make sure that the host is doing the same AddHeikenAshi() calls as those hosted scripts would. For further reference, please also review the 'Adding additional Bars Objects to NinjaScript' section in [Multi-Time Frame & Instruments](https://developer.ninjatrader.com/docs/desktop/multi_time_frame_instruments)
- Arguments supplied to AddHeikenAshi() should be hardcoded and NOT dependent on run-time variables which cannot be reliably obtained during [State.Configure](https://developer.ninjatrader.com/docs/desktop/state) (e.g., [Instrument](https://developer.ninjatrader.com/docs/desktop/instrument), [Bars](https://developer.ninjatrader.com/docs/desktop/bars), or user input). Attempting to add a data series dynamically is NOT guaranteed and therefore should be avoided. Trying to load bars dynamically may result in an error similar to: Unable to load bars series. Your NinjaScript may be trying to use an additional data series dynamically in an unsupported manner.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/addheikenashi#parameters)


| --- |
| instrumentName | A string determining instrument name such as "MSFT" |
| baseBarsPeriodType | The underlying BarsType used for the Heiken Ashi bars period. Possible values are: BarsPeriodType.Tick, BarsPeriodType.Volume, BarsPeriodType.Range, BarsPeriodType.Second, BarsPeriodType.Minute, BarsPeriodType.Day, BarsPeriodType.Week, BarsPeriodType.Month, BarsPeriodType.Year |
| baseBarsPeriodTypeValue | An int determining the underlying period interval such as "3" for 3 minute bars |
| marketDataType | The MarketDataType used for the bars object (last, bid, ask). Possible values are: MarketDataType.Ask, MarketDataType.Bid, MarketDataType.Last. Note: Please see the article [here](https://developer.ninjatrader.com/docs/desktop/using_historical_bid_ask_serie) on using Bid/Ask series. |
| tradingHoursName | A string determining the trading hours template for the instrument |
| isResetOnNewTradingDay | A nullable bool determining if the Bars object should [Break at EOD(https://ninjatrader.com/support/helpGuides/nt8/NT%20HelpGuide%20English.html?break_at_eod.htm). Will accept true, false or null as the input. If null is used, the data series will use the settings of the primary data series. |

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


You can optionally add the exchange name as a suffix to the symbol name. This is only advised if the instrument has multiple possible exchanges that it can trade on and it is configured within the Instruments window. For example: AddHeikenAshi("MSFT Arca", BarsPeriodType.Minute, 1, MarketDataType.Last);


---


## [Examples](https://developer.ninjatrader.com/docs/desktop/addheikenashi#examples)


```csharp
protected override void OnStateChange()
{
   if (State == State.SetDefaults)
   {
       Name = "Examples Indicator";
   }
   else if (State == State.Configure)
   {
       // Add a 1 minute Heiken Ashi Bars object for the ES 03-18 contract - BarsInProgress index = 1
       AddHeikenAshi("ES 03-18", BarsPeriodType.Minute, 1, MarketDataType.Last);
   }
}

protected override void OnBarUpdate()
{
     // Ignore the primary Bars object and only process the Heiken Ashi object
     if (BarsInProgress == 1)
     {
         // Do something;
     }
}
```
