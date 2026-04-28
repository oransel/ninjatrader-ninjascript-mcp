# IsTradingHoursBreakLineVisible

Source: https://developer.ninjatrader.com/docs/desktop/istradinghoursbreaklinevisible

---

# IsTradingHoursBreakLineVisible


## [Definition](https://developer.ninjatrader.com/docs/desktop/istradinghoursbreaklinevisible#definition)


Plots trading hours break lines on the indicator panel.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


The indicator panel's parent chart has a similar property **Plot session break line** which if set to false, will override the indicator's local setting if true.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/istradinghoursbreaklinevisible#property-value)


This property returns true if trading hours break lines are plotted on the indicator panel; otherwise, false. Default set to true.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


This property should ONLY be set from the **OnStateChange()** method during **State.SetDefaults** or **State.Configure**.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/istradinghoursbreaklinevisible#syntax)


`IsTradingHoursBreakLineVisible`


## [Examples](https://developer.ninjatrader.com/docs/desktop/istradinghoursbreaklinevisible#examples)


```csharp
protected override void OnStateChange()
{
    if (State == State.SetDefaults)
    {
        IsTradingHoursBreakLineVisible = true;
        AddPlot(Brushes.Orange, "SMA");
    }
}
```
