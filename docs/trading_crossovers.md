# Trading crossovers

Source: https://developer.ninjatrader.com/docs/desktop/trading_crossovers

---

# Trading crossovers


Similar in concept to a breakout, many traders like to trade crossovers. This can be a crossover of price from a certain threshold or even an indicator crossing over another indicator.


## [Key concepts in this example](https://developer.ninjatrader.com/docs/desktop/trading_crossovers#key-concepts-in-this-example)


- Determining and storing the first 15 bar high and low values for the current session
- Submitting long or short entry orders depending on which threshold is crossed
- Using a trail stop to exit positions
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Tip: This reference sample sets **Calculate** to **OnEachTick**. The reason we are doing this is so we can submit orders as soon as a crossover occurs instead of waiting for the bar to close before submitting the order.


## [Important related documentation](https://developer.ninjatrader.com/docs/desktop/trading_crossovers#important-related-documentation)


- [Calculate](https://developer.ninjatrader.com/docs/desktop/calculate)
- [CrossAbove()](https://developer.ninjatrader.com/docs/desktop/crossabove)
- [CrossBelow()](https://developer.ninjatrader.com/docs/desktop/crossbelow)
- [SetTrailStop()](https://developer.ninjatrader.com/docs/desktop/settrailstop)
- [SetStopLoss()](https://developer.ninjatrader.com/docs/desktop/setstoploss)
- [SetProfitTarget()](https://developer.ninjatrader.com/docs/desktop/setprofittarget)


## [Import instructions](https://developer.ninjatrader.com/docs/desktop/trading_crossovers#import-instructions)


- Download the file contained in this Help Guide topic to your PC desktop
- From the Control Center window, select the menu Tools > Import > NinjaScript
- Select the downloaded file


[SampleHighLowCross_NT8.zip](https://ninjatrader.com/support/helpGuides/nt8/samples/SampleHighLowCross_NT8.zip)
