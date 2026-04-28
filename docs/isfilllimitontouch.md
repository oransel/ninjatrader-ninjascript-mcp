# IsFillLimitOnTouch

Source: https://developer.ninjatrader.com/docs/desktop/isfilllimitontouch

---

# IsFillLimitOnTouch


## [Definition](https://developer.ninjatrader.com/docs/desktop/isfilllimitontouch#definition)


Determines if the strategy will use a more liberal fill algorithm for back-testing purposes only. The default behavior of the strategy's fill algorithm is to fill a limit order once price has penetrated the limit price. However, this behavior can be changed by setting **IsFillLimitOnTouch** to true, in which case the strategy's fill algorithm will consider a limit order filled once price has reached the limit price, but does not necessarily need to trade through the limit price.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/isfilllimitontouch#property-value)


This property returns true if the strategy will fill limit orders when touched; otherwise, false. Default is set to false.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


This property should ONLY be set from the **OnStateChange()** method during State.SetDefaults or State.Configure.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/isfilllimitontouch#syntax)


`IsFillLimitOnTouch`


## [Examples](https://developer.ninjatrader.com/docs/desktop/isfilllimitontouch#examples)


```csharp
protected override void OnStateChange()
{
    if (State == State.SetDefaults)
    {
        IsFillLimitOnTouch = true;
    }
}
```
