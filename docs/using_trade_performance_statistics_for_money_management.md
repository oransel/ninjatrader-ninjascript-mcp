# Using trade performance statistics for money management

Source: https://developer.ninjatrader.com/docs/desktop/using_trade_performance_statistics_for_money_management

---

# Using trade performance statistics for money management


For money management reasons you may want to limit your strategy from aggressive daytrading or you may want to cut your losses short on volatile sessions that are not playing out in your favor. This can be done through the utilization of the Performance object.


## [Key concepts in this example](https://developer.ninjatrader.com/docs/desktop/using_trade_performance_statistics_for_money_management#key-concepts-in-this-example)


- Locking in realized profits after a certain amount of gains have been achieved during the trading session
- Cutting realized losses short after a certain amount of losses have been accrued over the trading session
- Preventing aggressive amounts of trading


## [Important related documentation](https://developer.ninjatrader.com/docs/desktop/using_trade_performance_statistics_for_money_management#important-related-documentation)


- [SystemPerformance](https://developer.ninjatrader.com/docs/desktop/systemperformance)
- [TradeCollection](https://developer.ninjatrader.com/docs/desktop/tradecollection)
- [AllTrades*](https://developer.ninjatrader.com/docs/desktop/alltrades)


** This reference sample uses the **.AllTrades** property. This property will include all historical virtual trades as well as real-time trades. If you wish to only make calculations based on real-time trades you can use the **.RealtimeTrades** property.*


## [Import instructions](https://developer.ninjatrader.com/docs/desktop/using_trade_performance_statistics_for_money_management#import-instructions)


- Download the file contained in this Help Guide topic to your PC desktop
- From the Control Center window, select the menu Tools > Import > NinjaScript
- Select the downloaded file


[SamplePnL_NT8.zip](https://ninjatrader.com/support/helpGuides/nt8/samples/SamplePnL_NT8.zip)
