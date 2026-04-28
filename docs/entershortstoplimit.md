# EnterShortStopLimit()

Source: https://developer.ninjatrader.com/docs/desktop/entershortstoplimit

---

# EnterShortStopLimit()


## [Definition](https://developer.ninjatrader.com/docs/desktop/entershortstoplimit#definition)


Generates a sell short stop limit order to enter a short position.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/entershortstoplimit#method-return-value)


An **Order** read-only object that represents the order. Reserved for experienced programmers, additional information can be found within the [Advanced Order Handling](https://developer.ninjatrader.com/docs/desktop/advanced_order_handling) section.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/entershortstoplimit#syntax)


`EnterShortStopLimit(double limitPrice, double stopPrice)`


`EnterShortStopLimit(double limitPrice, double stopPrice, string signalName)`


`EnterShortStopLimit(int quantity, double limitPrice, double stopPrice)`


`EnterShortStopLimit(int quantity, double limitPrice, double stopPrice, string signalName)`


The following method variation is for experienced programmers who fully understand [Advanced Order Handling](https://developer.ninjatrader.com/docs/desktop/advanced_order_handling) concepts:


`EnterShortStopLimit(int barsInProgressIndex, bool isLiveUntilCancelled, int quantity, double limitPrice, double stopPrice, string signalName)`
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


If using a method signature that does not have the parameter quantity, the order quantity will be taken from the quantity value set in the strategy dialog window when running or backtesting a strategy.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/entershortstoplimit#parameters)


| --- |
| **signalName** | User defined signal name identifying the order generated. Max 50 characters. |
| **limitPrice** | The limit price of the order. |
| **stopPrice** | The stop price of the order. |
| **quantity** | Entry order quantity (if 0 is passed in, will be set to 1, except for stocks 100). |
| **isLiveUntilCancelled** | The order will NOT expire at the end of a bar, but instead remain live until the **CancelOrder()** method is called or its time in force is reached. |
| **barsInProgressIndex** | The index of the Bars object the order is to be submitted against. Used to determine what instrument the order is submitted for. See the **BarsInProgress** property. |


## [Examples](https://developer.ninjatrader.com/docs/desktop/entershortstoplimit#examples)


```csharp
protected override void OnBarUpdate()
{
     if (CurrentBar < 20)
         return;

     // Only enter if at least 10 bars has passed since our last entry
     if ((BarsSinceEntryExecution() > 10 || BarsSinceEntryExecution() == -1) && CrossAbove(SMA(10), SMA(20), 1))
         EnterShortStopLimit(Low[0] - 2 * TickSize, Low[0], "SMA Cross Entry");
}
```
