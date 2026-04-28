# IgnoreOverfill

Source: https://developer.ninjatrader.com/docs/desktop/ignoreoverfill

---

# IgnoreOverfill


## [Definition](https://developer.ninjatrader.com/docs/desktop/ignoreoverfill#definition)


An **unmanaged order property** which defines the behavior of a strategy when an overfill is detected. An overfill is categorized as when an order returns a "Filled" or "PartFilled" state after the order was already marked for cancellation. The cancel request could have been induced by an explicit **CancelOrder()** call, from more implicit cancellations like those that occur when another order sharing the same OCO ID is filled, or from things like order expiration.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


- Setting this property value to true can have serious adverse effects on a running strategy unless you have programmed your own overfill handling.
- User defined overfill handling is advanced and should ONLY be addressed by experienced programmers. Additional information can be found on overfills in the [Unmanaged approach](https://developer.ninjatrader.com/docs/desktop/unmanaged_approach).


## [Property Value](https://developer.ninjatrader.com/docs/desktop/ignoreoverfill#property-value)


This property returns true if the strategy will ignore overfills; otherwise, false. Default is set to false.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


This property should ONLY be set from the **OnStateChange()** method during State.SetDefaults or State.Configure.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/ignoreoverfill#syntax)


`IgnoreOverfill`


## [Examples](https://developer.ninjatrader.com/docs/desktop/ignoreoverfill#examples)


```csharp
protected override void OnStateChange()
{
    if (State == State.SetDefaults)
    {
        // Allows for custom overfill handling
        IgnoreOverfill = true;
    }
}
```
