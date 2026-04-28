# CancelOrder()

Source: https://developer.ninjatrader.com/docs/desktop/cancelorder

---

# CancelOrder()


## [Definition](https://developer.ninjatrader.com/docs/desktop/cancelorder#definition)


Cancels a specified order. This method is reserved for experienced programmers that fully understand the concepts of advanced order handling.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Notes:


- This method sends a cancel request to the broker and does not guarantee that an order is completely cancelled. Most of the time you can expect your order to come back 100% cancelled.
- An order can be completely filled or part filled in the time that you send the cancel request and the time the exchange receives the request. Check the **OnOrderUpdate()** method for the state of an order you attempted to cancel.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/cancelorder#syntax)


`CancelOrder(Order order)`
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


Warning: If you have existing historical `order` references which have transitioned to real-time, you MUST update the order object reference to the newly submitted real-time order; otherwise errors may occur as you attempt to cancel the order. You may use the `GetRealtimeOrder()` helper method to assist in this transition.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/cancelorder#parameters)


| Parameter | Description |
| --- | --- |
| **order** | An **Order** object representing the order you wish to cancel. |


## [Examples](https://developer.ninjatrader.com/docs/desktop/cancelorder#examples)


```csharp
private Order myEntryOrder = null;
private int barNumberOfOrder = 0;

protected override void OnBarUpdate()
{
    // Submit an entry order at the low of a bar
    if (myEntryOrder == null)
    {
        // use 'live until canceled' limit order to prevent default managed order handling which would expire at end of bar
        EnterLongLimit(0, true, 1, Low[0], "Long Entry");
        barNumberOfOrder = CurrentBar;
    }

    // If more than 5 bars has elapsed, cancel the entry order
    if (CurrentBar > barNumberOfOrder + 5)
        CancelOrder(myEntryOrder);
}

protected override void OnOrderUpdate(Order order, double limitPrice, double stopPrice, int quantity, int filled,
    double averageFillPrice, OrderState orderState, DateTime time, ErrorCode error, string nativeError)
{
    // Assign entryOrder in OnOrderUpdate() to ensure the assignment occurs when expected.
    // This is more reliable than assigning Order objects in OnBarUpdate, as the assignment is not guaranteed to be complete if it is referenced immediately after submitting
    if (order.Name == "Long Entry")
        myEntryOrder = order;

    // Evaluates for all updates to myEntryOrder.
    if (myEntryOrder != null && myEntryOrder == order)
    {
        // Check if myEntryOrder is cancelled.
        if (myEntryOrder.OrderState == OrderState.Cancelled)
        {
            // Reset myEntryOrder back to null
            myEntryOrder = null;
        }
    }
}
```
