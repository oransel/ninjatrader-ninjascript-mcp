# PercentComplete

Source: https://developer.ninjatrader.com/docs/desktop/percentcomplete

---

# PercentComplete


## [Definition](https://developer.ninjatrader.com/docs/desktop/percentcomplete#definition)


Returns a value indicating the percentage complete of the real-time bar processing.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Notes:


- Since a historical bar is complete, values during State.Historical should be ignored (also the case with **TickReplay** bars).
- Some [BarsTypes](https://developer.ninjatrader.com/docs/desktop/bars_type) may not be compatible with the `PercentComplete` property. In these cases, a value of 0 always returns (e.g., **Range**, **Renko**, **Point & Figure**, **Kagi**, **LineBreak**, and some other 3rd party bars types).


## [Property Value](https://developer.ninjatrader.com/docs/desktop/percentcomplete#property-value)


A **double** value representing a percent e.g. a value of .5 indicates the bar was at 50%. This property is read-only.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/percentcomplete#syntax)


`Bars.PercentComplete`
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Tip: If you are developing a custom `BarsType`, please use the [GetPercentComplete()](https://developer.ninjatrader.com/docs/desktop/getpercentcomplete) method used to calculate the value returned by **PercentComplete**.


## [Examples](https://developer.ninjatrader.com/docs/desktop/percentcomplete#examples)


```csharp
protected override void OnBarUpdate()
{
    if(State == State.Realtime)
    {
        Draw.TextFixed(this, "barstatus", Bars.PercentComplete.ToString("P2"), TextPosition.BottomRight);
    }
}
```
