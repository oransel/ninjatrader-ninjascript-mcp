# Keeping orders alive

Source: https://developer.ninjatrader.com/docs/desktop/keeping_orders_alive

---

# Keeping orders alive


The default behavior for **NinjaTrader** is to cancel limit orders if the trigger conditions are no longer true. It is possible to submit orders that stay active until cancelled by setting **liveUntilCancelled** to true. This sample demonstrates and explains the difference between submitting an order with **isLiveUntilCancelled** true and false. The comments contain a longer, more detailed explanation.


## [Key concepts in this example](https://developer.ninjatrader.com/docs/desktop/keeping_orders_alive#key-concepts-in-this-example)


- How to submit an order that stays active until it is explicitly canceled
- Another sample demonstrating how to explicitly cancel orders can be found here: [Using CancelOrder() method to cancel orders](https://developer.ninjatrader.com/docs/desktop/using_cancelorder_method_to_ca)


## [Important related documentation](https://developer.ninjatrader.com/docs/desktop/keeping_orders_alive#important-related-documentation)


- [EnterLongLimit()](https://developer.ninjatrader.com/docs/desktop/enterlonglimit)
- [isliveUntilCancelled](https://developer.ninjatrader.com/docs/desktop/exitlonglimit)
- [CrossAbove()](https://developer.ninjatrader.com/docs/desktop/crossabove)
- [CrossBelow()](https://developer.ninjatrader.com/docs/desktop/crossbelow)


## [Import instructions](https://developer.ninjatrader.com/docs/desktop/keeping_orders_alive#import-instructions)


- Download the file contained in this Help Guide topic to your PC desktop
- From the Control Center window, select the menu Tools > Import > NinjaScript
- Select the downloaded file


[SampleIsLiveUntilCanceled_NT8.zip](https://ninjatrader.com/support/helpGuides/nt8/samples/SampleIsLiveUntilCanceled_NT8.zip)
