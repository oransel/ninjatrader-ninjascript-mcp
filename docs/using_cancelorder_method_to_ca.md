# Using CancelOrder() method to cancel orders

Source: https://developer.ninjatrader.com/docs/desktop/using_cancelorder_method_to_ca

---

# Using CancelOrder() method to cancel orders


When using NinjaTrader's Entry and Exit methods, the default behavior is to automatically expire them at the end of a bar unless they are resubmitted to keep them alive. Sometimes you may want more flexibility in this behavior and wish to submit orders as live-until-cancelled. When orders are submitted as live-until-cancelled, the way to cancel them is by using the [CancelOrder()](https://developer.ninjatrader.com/docs/desktop/cancelorder) method.


## [Key concepts in this example](https://developer.ninjatrader.com/docs/desktop/using_cancelorder_method_to_ca#key-concepts-in-this-example)


- Submitting live-until-cancelled entry orders
- Manually cancelling orders


## [Important related documentation](https://developer.ninjatrader.com/docs/desktop/using_cancelorder_method_to_ca#important-related-documentation)


- [CancelOrder()](https://developer.ninjatrader.com/docs/desktop/cancelorder)
- [Order](https://developer.ninjatrader.com/docs/desktop/order)
- [OnOrderUpdate()](https://developer.ninjatrader.com/docs/desktop/onorderupdate)
- [OnExecutionUpdate()](https://developer.ninjatrader.com/docs/desktop/onexecutionupdate)
- [EnterLongLimit()](https://developer.ninjatrader.com/docs/desktop/enterlonglimit)


## [Import instructions](https://developer.ninjatrader.com/docs/desktop/using_cancelorder_method_to_ca#import-instructions)


- Download the file contained in this Help Guide topic to your PC desktop
- From the Control Center window, select the menu Tools > Import > NinjaScript
- Select the downloaded file


[SampleCancelOrder_NT8.zip](https://ninjatrader.com/support/helpGuides/nt8/samples/SampleCancelOrder_NT8.zip)
