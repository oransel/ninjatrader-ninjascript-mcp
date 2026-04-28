# TraceOrders

Source: https://developer.ninjatrader.com/docs/desktop/traceorders2

---

# TraceOrders


[TraceOrders](https://developer.ninjatrader.com/docs/desktop/traceorders) is a useful property when debugging the behavior of your orders. With the use of this property, you can track orders placed, amended, and canceled. The traces displayed in the NinjaScript Output window or if used, in the **OnOrderTrace** Override in the script where this was set. This will provide meaningful information for diagnosis when NinjaTrader ignores, changes or cancels orders when various strategy order methods are called.


To enable **TraceOrders**, add this line into the **OnStateChange()** method in the state SetDefaults of your NinjaScript strategy:


```csharp
protected override void OnStateChange()
{
     if (State == State.SetDefaults)
     {
         TraceOrders = true;
     }
}
```


Trace output examples:
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This trace is outputted when we place an entry order. It tells us all the pertaining properties of our order as well as the time it was submitted.


```csharp
Entered internal **SubmitOrderManaged()** method at 6/2/2015 8:42:00 AM: BarsInProgress=0 Action=Buy OrderType=Market Quantity=1 LimitPrice=0 StopPrice=0 SignalName='market order' FromEntrySignal=''
```

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This trace tells us that a previously submitted order was modified instead of submitting a completely new order.


```csharp
Amended open order at 6/2/2015 11:39:00 AM: BarsInProgress=0 Action=Buy OrderType=Limit Quantity=1 LimitPrice=130.41 StopPrice=0 SignalName='long order to be resubmitted' FromEntrySignal=''
```

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This trace provides the reason why our Limit order was ignored.


```csharp
Ignored **SubmitOrderManaged()** method at 6/2/2015 12:55:00 PM: BarsInProgress=0 Action=Buy OrderType=Limit Quantity=1 LimitPrice=129.92 StopPrice=0 SignalName='long order to be resubmitted' FromEntrySignal='' Reason='Exceeded entry signals limit based on EntryHandling and EntriesPerDirection properties'
```

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This trace tells us that our Limit order was canceled because it had expired.


```csharp
Cancelled expired order: BarsInProgress=0, orderId='NT-00123-118' account='Sim101' name='long order to be resubmitted' orderState=Working instrument='AAPL' orderAction=Buy orderType='Limit' limitPrice=130.3 stopPrice=0 quantity=1 tif=Gtc oco='' filled=0 averageFillPrice=0 id=-1 gtd='2099-12-01'
```


A new concept in NinjaTrader 8 is the [OnOrderTrace](https://developer.ninjatrader.com/docs/desktop/onordertrace) override method.


This method prevents **TraceOrders** from printing the traces directly to the output window but instead sends this information to the **OnOrderTrace** override where you can do logic or format the trace how you would like and then print only what you need to see.


```csharp
protected override void OnOrderTrace(DateTime timestamp, string message)
{
     Print(string.Format("{0} {1}", timestamp, message));
}
```


These examples illustrate the most common traces you will run across. They are mostly useful in determining the reason your orders are not submitted or cancelled. **TraceOrders** will only show you what is happening under the hood when you submit orders, but it will not tell you what happens after the order is submitted. To determine the behavior of your orders after submission you will need to look into your NinjaTrader trace logs. You can view those either through the "Log" tab on the "Control Center" or from the trace folder in My Documents\NinjaTrader 8\trace.


For more information on how to debug your NinjaScript please review the [Debugging](https://developer.ninjatrader.com/docs/desktop/debugging_your_ninjascript_code) tip.
