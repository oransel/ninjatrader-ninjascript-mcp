# TraceOrders

Source: https://developer.ninjatrader.com/docs/desktop/traceorders

---

# TraceOrders


## [Definition](https://developer.ninjatrader.com/docs/desktop/traceorders#definition)


Determines if **OnOrderTrace()** would be called for a given strategy. When enabled, traces are generated and displayed in the [NinjaScript Output](https://ninjatrader.com/support/helpGuides/nt8/?output.htm) window for each call of an **order method** providing confirmation that the method is entered and providing information if order methods are ignored and why. This is valuable for debugging if you are not seeing expected behavior when calling an order method. This property can be set programmatically in the **OnStateChange()** method.


The output will reference a method **PlaceOrder()** which is an internal method that all **Enter()** and **Exit()** methods use.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/traceorders#property-value)


This property returns true if the strategy will output trace information; otherwise, false. Default value is false.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/traceorders#syntax)


`TraceOrders`


## [Examples](https://developer.ninjatrader.com/docs/desktop/traceorders#examples)


```csharp
protected override void OnStateChange()
{
     if (State == State.SetDefaults)
     {
         TraceOrders = true;
     }
}
```

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Tips


- See [this](https://developer.ninjatrader.com/docs/desktop/traceorders2) article for more examples of how to utilize this property.
- You can override the default output by using **OnOrderTrace()** in your strategy.
