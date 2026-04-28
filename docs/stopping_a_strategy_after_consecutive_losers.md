# Stopping a strategy after consecutive losers

Source: https://developer.ninjatrader.com/docs/desktop/stopping_a_strategy_after_consecutive_losers

---

# Stopping a strategy after consecutive losers


Trending days or ranging days can make or break a strategy. If you have a system that does extremely well on trending days, you may look for a way to turn that system off during range-bound days. A simple filter you may use could be something like, "If the last three trades were consecutive losers, stop trading for the rest of the session."


## [Key concepts in this example](https://developer.ninjatrader.com/docs/desktop/stopping_a_strategy_after_consecutive_losers#key-concepts-in-this-example)


- Obtaining previous trade information to decide whether or not to keep trading for the day


## [Important related documentation](https://developer.ninjatrader.com/docs/desktop/stopping_a_strategy_after_consecutive_losers#important-related-documentation)


- [SystemPerformance](https://developer.ninjatrader.com/docs/desktop/systemperformance)
- [TradeCollection](https://developer.ninjatrader.com/docs/desktop/tradecollection)
- [AllTrades*](https://developer.ninjatrader.com/docs/desktop/alltrades)
- [EnterLong()](https://developer.ninjatrader.com/docs/desktop/enterlong)
- [ExitLong()](https://developer.ninjatrader.com/docs/desktop/exitlong)
- [IsFirstBarOfSession](https://developer.ninjatrader.com/docs/desktop/isfirstbarofsession)
- [IsFirstTickOfBar](https://developer.ninjatrader.com/docs/desktop/isfirsttickofbar)
- *This reference sample uses the **.AllTrades** property. This property will include all historical virtual trades as well as real-time trades. If you wish to only make calculations based on real-time trades you can use the **.RealtimeTrades** property.*


## [Import instructions](https://developer.ninjatrader.com/docs/desktop/stopping_a_strategy_after_consecutive_losers#import-instructions)


- Download the file contained in this Help Guide topic to your PC desktop.
- From the Control Center window, select the menu Tools > Import > NinjaScript.
- Select the downloaded file.


[SampleTradeObjects_Nt8.zip](https://ninjatrader.com/support/helpGuides/nt8/samples/SampleTradeObjects_Nt8.zip)
