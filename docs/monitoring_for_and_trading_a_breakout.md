# Monitoring for and trading a breakout

Source: https://developer.ninjatrader.com/docs/desktop/monitoring_for_and_trading_a_breakout

---

# Monitoring for and trading a breakout


A common concept many traders use is the idea of a breakout. Points of interest are when the price breaks out from a consolidation range or from previous highs and lows.


## [Key concepts in this example](https://developer.ninjatrader.com/docs/desktop/monitoring_for_and_trading_a_breakout#key-concepts-in-this-example)


- Determining and storing the first 30 bar high
- Submitting a long stop order to be filled when price breaks out from the 30 bar high
- Closing positions after a certain amount of bars have passed
- Resetting the 30 bar high at the start of every new trading session


## [Important related documentation](https://developer.ninjatrader.com/docs/desktop/monitoring_for_and_trading_a_breakout#important-related-documentation)


- [IsFirstBarOfSession](https://developer.ninjatrader.com/docs/desktop/isfirstbarofsession)
- [BarsSinceNewTradingDay](https://developer.ninjatrader.com/docs/desktop/barssincenewtradingday)
- [BarsSinceEntryExecution()](https://developer.ninjatrader.com/docs/desktop/barssinceentryexecution)
- [BarsSinceExitExecution()](https://developer.ninjatrader.com/docs/desktop/barssinceexitexecution)


## [Import instructions](https://developer.ninjatrader.com/docs/desktop/monitoring_for_and_trading_a_breakout#import-instructions)


- Download the file contained in this Help Guide topic to your PC desktop
- From the Control Center window, select the menu Tools > Import > NinjaScript
- Select the downloaded file


[SampleBreakoutStrategy_NT8.zip](https://ninjatrader.com/support/helpGuides/nt8/samples/SampleBreakoutStrategy_NT8.zip)
