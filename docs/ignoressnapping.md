# IgnoresSnapping

Source: https://developer.ninjatrader.com/docs/desktop/ignoressnapping

---

# IgnoresSnapping


## [Definition](https://developer.ninjatrader.com/docs/desktop/ignoressnapping#definition)


Determines if the drawing tool chart anchor's will use the chart's Snap Mode mouse coordinates.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/ignoressnapping#property-value)


A bool value which when true the drawing tool ignores snapping; otherwise false. Default is set to false.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/ignoressnapping#syntax)


`IgnoresSnapping`


## [Examples](https://developer.ninjatrader.com/docs/desktop/ignoressnapping#examples)


```csharp
protected override void OnStateChange()
{
     if (State == State.SetDefaults)
     {
          IgnoresSnapping = true; // Set this to true to receive non-snapped mouse coordinates
     }
     else if (State == State.Configure)
     {

     }
}
```
