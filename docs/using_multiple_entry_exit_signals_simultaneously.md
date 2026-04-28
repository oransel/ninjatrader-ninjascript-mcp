# Using multiple entry-exit signals simultaneously

Source: https://developer.ninjatrader.com/docs/desktop/using_multiple_entry_exit_signals_simultaneously

---

# Using multiple entry-exit signals simultaneously


Sometimes you want to trade an instrument with several different possible entry conditions. To keep track of which trade used which conditions can become cumbersome if done on paper.


## [The attached reference sample demonstrates the following key concepts](https://developer.ninjatrader.com/docs/desktop/using_multiple_entry_exit_signals_simultaneously#the-attached-reference-sample-demonstrates-the-following-key-concepts)


- Adding user definable indicators to the strategy for display on the chart
- Setting the manner in which NinjaTrader handles entry orders
- Using unique identifiers for entry and exit orders


## [Important methods and properties used include](https://developer.ninjatrader.com/docs/desktop/using_multiple_entry_exit_signals_simultaneously#important-methods-and-properties-used-include)


- [AddChartIndicator()](https://developer.ninjatrader.com/docs/desktop/addchartindicator)
- [EntriesPerDirection*](https://developer.ninjatrader.com/docs/desktop/entriesperdirection)
- [EntryHandling*](https://developer.ninjatrader.com/docs/desktop/entryhandling)


**Entry handling properties can be either programmatically set or set through the Strategy dialog window*


## [Other methods and properties of interest include](https://developer.ninjatrader.com/docs/desktop/using_multiple_entry_exit_signals_simultaneously#other-methods-and-properties-of-interest-include)


- [EnterLongLimit()](https://developer.ninjatrader.com/docs/desktop/enterlonglimit)
- [EnterLongStopMarket()](https://developer.ninjatrader.com/docs/desktop/enterlongstopmarket)
- [EnterLongStopLimit()](https://developer.ninjatrader.com/docs/desktop/enterlongstoplimit)


## [Import instructions](https://developer.ninjatrader.com/docs/desktop/using_multiple_entry_exit_signals_simultaneously#import-instructions)


- Download the file contained in this Help Guide topic to your PC desktop
- From the Control Center window, select the menu Tools > Import > NinjaScript
- Select the downloaded file


[SampleMultipleEntryExitSignals_NT8.zip](https://ninjatrader.com/support/helpGuides/nt8/samples/SampleMultipleEntryExitSignals_NT8.zip)
