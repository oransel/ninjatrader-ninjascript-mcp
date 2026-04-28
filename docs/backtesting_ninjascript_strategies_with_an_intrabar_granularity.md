# Backtesting NinjaScript Strategies with an intrabar granularity

Source: https://developer.ninjatrader.com/docs/desktop/backtesting_ninjascript_strategies_with_an_intrabar_granularity

---

# Backtesting NinjaScript Strategies with an intrabar granularity


You can submit orders to different Bars objects. This allows you the flexibility of submitting orders to different timeframes. Like in live trading, taking entry conditions from a 5min chart means executing your order as soon as possible instead of waiting until the next 5min bar starts building. You can achieve this by submitting your orders to a more granular secondary bar series to achieve an "intrabar" fill.


## [Key concepts in this example](https://developer.ninjatrader.com/docs/desktop/backtesting_ninjascript_strategies_with_an_intrabar_granularity#key-concepts-in-this-example)


- Finding entry conditions on the primary bar object
- Submitting orders to the secondary bar object for an intrabar fill


## [Important related documentation](https://developer.ninjatrader.com/docs/desktop/backtesting_ninjascript_strategies_with_an_intrabar_granularity#important-related-documentation)


- [AddDataSeries()](https://developer.ninjatrader.com/docs/desktop/adddataseries)
- [BarsInProgress](https://developer.ninjatrader.com/docs/desktop/barsinprogress)
- [EnterLong()](https://developer.ninjatrader.com/docs/desktop/enterlong)
- [BarsArray](https://developer.ninjatrader.com/docs/desktop/barsarray)
- [EnterLongLimit()](https://developer.ninjatrader.com/docs/desktop/enterlonglimit)


## [Import instructions](https://developer.ninjatrader.com/docs/desktop/backtesting_ninjascript_strategies_with_an_intrabar_granularity#import-instructions)


- Download the file contained in this Help Guide topic to your PC desktop
- From the Control Center window, select the menu Tools > Import > NinjaScript
- Select the downloaded file


[SampleIntrabarBacktest_NT8.zip](https://ninjatrader.com/support/helpGuides/nt8/samples/SampleIntrabarBacktest_NT8.zip)
