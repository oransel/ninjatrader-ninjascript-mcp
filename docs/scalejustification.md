# ScaleJustification

Source: https://developer.ninjatrader.com/docs/desktop/scalejustification

---

# ScaleJustification


## [Definition](https://developer.ninjatrader.com/docs/desktop/scalejustification#definition)


Determines which scale an indicator will be plotted on.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


This property should ONLY be set from the **OnStateChange()** method during **State.SetDefaults** or **State.Configure**.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/scalejustification#property-value)


This property returns a **ScaleJustification** value of either:


- **NinjaTrader.Gui.Charts.ScaleJustification.Left**
- **NinjaTrader.Gui.Charts.ScaleJustification.Overlay**
- **NinjaTrader.Gui.Charts.ScaleJustification.Right**


## [Syntax](https://developer.ninjatrader.com/docs/desktop/scalejustification#syntax)


`ScaleJustification`


## [Examples](https://developer.ninjatrader.com/docs/desktop/scalejustification#examples)


```csharp
protected override void OnStateChange()
{
   if (State == State.SetDefaults)
   {
     Name = "Examples Indicator";

     // force "My Plot" to be plotted on the left scale
     ScaleJustification = ScaleJustification.Left;
   }
   else if (State == State.Configure)
   {
     AddPlot(Brushes.Orange, "My Plot");
   }
}
```
