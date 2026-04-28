# OrderFillResolution

Source: https://developer.ninjatrader.com/docs/desktop/orderfillresolution

---

# OrderFillResolution


## [Definition](https://developer.ninjatrader.com/docs/desktop/orderfillresolution#definition)


Determines how strategy orders are filled during historical states.


Please see [Understanding Historical Fill Processing](https://ninjatrader.com/support/helpguides/nt8/?understanding_historical_fill_.htm) for general information on historical fill processing.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/orderfillresolution#property-value)


An enum value that determines how the strategy orders are filled. Default value is set to **OrderFillResolution.Standard**. Possible values are:


- **OrderFillResolution.Standard** - Faster - Uses the existing bar type and interval that you are running the backtest on to fill your orders.
- **OrderFillResolution.High** - More granular - Allows you to set a secondary bar series to be used as the price data to fill your orders. (See also [OrderFillResolutionType](https://developer.ninjatrader.com/docs/desktop/orderfillresolutiontype) and [OrderFillResolutionValue](https://developer.ninjatrader.com/docs/desktop/orderfillresolutionvalue))


## [Syntax](https://developer.ninjatrader.com/docs/desktop/orderfillresolution#syntax)


`OrderFillResolution`
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


This property should ONLY be set from the [OnStateChange()](https://developer.ninjatrader.com/docs/desktop/onstatechange) method during State.SetDefaults


## [Examples](https://developer.ninjatrader.com/docs/desktop/orderfillresolution#examples)


```csharp
protected override void OnStateChange()
{
   if (State == State.SetDefaults)
   {
     Name = "ExampleStrategy";
     OrderFillResolution = OrderFillResolution.Standard;
   }
}
```
