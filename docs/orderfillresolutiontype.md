# OrderFillResolutionType

Source: https://developer.ninjatrader.com/docs/desktop/orderfillresolutiontype

---

# OrderFillResolutionType


## [Definition](https://developer.ninjatrader.com/docs/desktop/orderfillresolutiontype#definition)


Determines the bars type which will be used for historical fill processing.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This property will only be valid if the **OrderFillResolution** is set to **OrderFillResolution.High**.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/orderfillresolutiontype#property-value)


A **BarsPeriodType** representing the type of bars during historical order processing. Default value is set to **BarsPeriodType.Minute**.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/orderfillresolutiontype#syntax)


`OrderFillResolutionType`
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


This property should ONLY be set from the `OnStateChange()` method during **State.SetDefaults**.


## [Examples](https://developer.ninjatrader.com/docs/desktop/orderfillresolutiontype#examples)


```csharp
protected override void OnStateChange()
{
    if (State == State.SetDefaults)
    {
        Name = "ExampleStrategy";

        // use one second bars for filling orders
        OrderFillResolution       = OrderFillResolution.High;
        OrderFillResolutionType   = BarsPeriodType.Second;
        OrderFillResolutionValue   = 1;
    }
}
```
