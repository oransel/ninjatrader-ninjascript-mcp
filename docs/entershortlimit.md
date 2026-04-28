# EnterShortLimit()

Source: https://developer.ninjatrader.com/docs/desktop/entershortlimit

---

# EnterShortLimit()


## [Definition](https://developer.ninjatrader.com/docs/desktop/entershortlimit#definition)


Generates a sell short limit order to enter a short position.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/entershortlimit#method-return-value)


An **Order** read-only object that represents the order. Reserved for experienced programmers, additional information can be found within the [Advanced Order Handling](https://developer.ninjatrader.com/docs/desktop/advanced_order_handling) section.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/entershortlimit#syntax)


`EnterShortLimit(double limitPrice)`


`EnterShortLimit(double limitPrice, string signalName)`


`EnterShortLimit(int quantity, double limitPrice)`


`EnterShortLimit(int quantity, double limitPrice, string signalName)`


The following method variation is for experienced programmers who fully understand [Advanced Order Handling](https://developer.ninjatrader.com/docs/desktop/advanced_order_handling) concepts:


`EnterShortLimit(int barsInProgressIndex, bool isLiveUntilCancelled, int quantity, double limitPrice, string signalName)`
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


If using a method signature that does not have the parameter quantity, the order quantity will be taken from the quantity value set in the strategy dialog window when running or backtesting a strategy.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/entershortlimit#parameters)


| Parameter | Description |
| --- | --- |
| signalName | User defined signal name identifying the order generated. Max 50 characters. |
| limitPrice | The limit price of the order. |
| quantity | Entry order quantity (if 0 is passed in, will be set to 1, except for stocks 100). |
| isLiveUntilCancelled | The order will NOT expire at the end of a bar, but instead remain live until the **CancelOrder()** method is called or its time in force is reached. |
| barsInProgressIndex | The index of the Bars object the order is to be submitted against. Used to determine what instrument the order is submitted for. See the [BarsInProgress](https://developer.ninjatrader.com/docs/desktop/barsinprogress) property. |


## [Examples](https://developer.ninjatrader.com/docs/desktop/entershortlimit#examples)


```csharp
protected override void OnBarUpdate()
{
     if (CurrentBar < 20)
         return;

     // Only enter if at least 10 bars has passed since our last entry
     if ((BarsSinceEntryExecution() > 10 || BarsSinceEntryExecution() == -1) && CrossAbove(SMA(10), SMA(20), 1))
         EnterShortLimit(GetCurrentAsk(), "SMA Cross Entry");
}
```
