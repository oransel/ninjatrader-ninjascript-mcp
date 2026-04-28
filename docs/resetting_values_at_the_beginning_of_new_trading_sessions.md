# Resetting values at the beginning of new trading sessions

Source: https://developer.ninjatrader.com/docs/desktop/resetting_values_at_the_beginning_of_new_trading_sessions

---

# Resetting values at the beginning of new trading sessions


Normally calculated values are carried over between trading sessions, but sometimes you may want to reset these values to begin a trading session fresh. The technique demonstrated in this reference sample can be useful to do things like resetting counters you may be running or clearing bool flags you may have set.


## [Key concepts in this example](https://developer.ninjatrader.com/docs/desktop/resetting_values_at_the_beginning_of_new_trading_sessions#key-concepts-in-this-example)


- Resetting a variable at the beginning of a new trading session
- Limiting the number of trades a strategy can make per trading session


## [Important related documentation](https://developer.ninjatrader.com/docs/desktop/resetting_values_at_the_beginning_of_new_trading_sessions#important-related-documentation)


- [IsFirstBarOfSession](https://developer.ninjatrader.com/docs/desktop/isfirstbarofsession)
- [IsFirstTickOfBar](https://developer.ninjatrader.com/docs/desktop/isfirsttickofbar)
- [EnterLong()](https://developer.ninjatrader.com/docs/desktop/enterlong)
- [ExitLong()](https://developer.ninjatrader.com/docs/desktop/exitlong)


## [Import instructions](https://developer.ninjatrader.com/docs/desktop/resetting_values_at_the_beginning_of_new_trading_sessions#import-instructions)


- Download the file contained in this Help Guide topic to your PC desktop
- From the Control Center window, select the menu Tools > Import > NinjaScript
- Select the downloaded file


[SampleTradeLimiter_NT8.zip](https://ninjatrader.com/support/helpGuides/nt8/samples/SampleTradeLimiter_NT8.zip)
