# Rounding values to the nearest tick size

Source: https://developer.ninjatrader.com/docs/desktop/rounding_values_to_the_nearest_tick_size

---

# Rounding values to the nearest tick size


When NinjaTrader receives a request to submit an order, it automatically rounds any limit price or stop price to the nearest tick for that specific instrument.


When debugging and/or printing out order information, this may not be apparent. NinjaTrader includes a Method named **RoundToTickSize** to apply the same internal rounding to any value you wish, which can help make comparisons easier.


## [Key concepts in this example](https://developer.ninjatrader.com/docs/desktop/rounding_values_to_the_nearest_tick_size#key-concepts-in-this-example)


- Rounding a value to the nearest tick


## [Important related documentation](https://developer.ninjatrader.com/docs/desktop/rounding_values_to_the_nearest_tick_size#important-related-documentation)


- [RoundToTickSize()](https://developer.ninjatrader.com/docs/desktop/roundtoticksize)
- [EnterLongLimit()](https://developer.ninjatrader.com/docs/desktop/enterlonglimit)
- [ExitLong()](https://developer.ninjatrader.com/docs/desktop/exitlong)
- [CrossAbove()](https://developer.ninjatrader.com/docs/desktop/crossabove)
- [CrossBelow()](https://developer.ninjatrader.com/docs/desktop/crossbelow)


## [Import instructions](https://developer.ninjatrader.com/docs/desktop/rounding_values_to_the_nearest_tick_size#import-instructions)


- Download the file contained in this Help Guide topic to your PC desktop
- From the Control Center window, select the menu Tools > Import > NinjaScript
- Select the downloaded file


[SampleRoundToTickSize_NT8.zip](https://ninjatrader.com/support/helpGuides/nt8/samples/SampleRoundToTickSize_NT8.zip)
