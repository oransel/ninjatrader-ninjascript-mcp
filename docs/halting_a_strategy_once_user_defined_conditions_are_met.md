# Halting a Strategy Once User Defined Conditions Are Met

Source: https://developer.ninjatrader.com/docs/desktop/halting_a_strategy_once_user_defined_conditions_are_met

---

# Halting a Strategy Once User Defined Conditions Are Met


For error-handling, money-management or any other reason you may want to halt your strategy from processing its core program logic. Before you halt your strategy, it is best to close all positions and cancel all active orders to prevent the risk of having an unmanaged position in the market. We have provided two reference samples for these topics.


## [Key concepts in the SampleHaltBasicStrategy example](https://developer.ninjatrader.com/docs/desktop/halting_a_strategy_once_user_defined_conditions_are_met#key-concepts-in-the-samplehaltbasicstrategy-example)


- Using **PnL** statistics to determine when to halt processing of the strategy
- Cancelling active orders
- Closing active positions


## [Key concepts in the SampleHaltAdvancedStrategy example](https://developer.ninjatrader.com/docs/desktop/halting_a_strategy_once_user_defined_conditions_are_met#key-concepts-in-the-samplehaltadvancedstrategy-example)


- Using a custom method to halt processing on all event-driven methods
- Advanced order handling in error situations with the **OnOrderUpdate()** method
- This is intended for strategies driven exclusively by the **OnBarUpdate()** method.
- This sample's intended audience is for advanced programmers who have programmed strategies that take advantage of event-driven methods such as, but not limited to, **OnMarketData()** or **OnOrderUpdate()** in addition to the **OnBarUpdate()** method.


## [Important related documentation](https://developer.ninjatrader.com/docs/desktop/halting_a_strategy_once_user_defined_conditions_are_met#important-related-documentation)


- [CancelOrder()](https://developer.ninjatrader.com/docs/desktop/cancel)
- [Order](https://developer.ninjatrader.com/docs/desktop/order)
- [SystemPerformance](https://developer.ninjatrader.com/docs/desktop/systemperformance)
- [AllTrades](https://developer.ninjatrader.com/docs/desktop/alltrades)
- [TradesPerformance](https://developer.ninjatrader.com/docs/desktop/tradesperformance)
- [OnMarketData()](https://developer.ninjatrader.com/docs/desktop/onmarketdata)
- [OnOrderUpdate()](https://developer.ninjatrader.com/docs/desktop/onorderupdate)
- This reference sample uses the **.AllTrades** property. This property will include all historical virtual trades as well as real-time trades. If you wish to only make calculations based on real-time trades you can use the **.RealtimeTrades** property.


## [Import instructions](https://developer.ninjatrader.com/docs/desktop/halting_a_strategy_once_user_defined_conditions_are_met#import-instructions)


- Download the file contained in this Help Guide topic to your PC desktop
- From the Control Center window, select the menu Tools > Import > NinjaScript
- Select the downloaded file


[SampleHaltAdvancedStrategy_NT8.zip](https://ninjatrader.com/support/helpGuides/nt8/samples/SampleHaltAdvancedStrategy_NT8.zip)


[SampleHaltBasicStrategy_NT8.zip](https://ninjatrader.com/support/helpGuides/nt8/samples/SampleHaltBasicStrategy_NT8.zip)
