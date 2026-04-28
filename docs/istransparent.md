# IsTransparent

Source: https://developer.ninjatrader.com/docs/desktop/istransparent

---

# IsTransparent


## [Definition](https://developer.ninjatrader.com/docs/desktop/istransparent#definition)


Indicates the bars in the ChartStyle are transparent.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/istransparent#property-value)


A bool which, when true, indicates that the **UpBrush**, **DownBrush**, and **Stroke.Brush** are all set to transparent. Returns false if any of the three are not transparent.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/istransparent#syntax)


`IsTransparent`


## [Examples](https://developer.ninjatrader.com/docs/desktop/istransparent#examples)


```csharp
protected override void OnStateChange()
{
   if (State == State.Configure)
   {
       //Print a message if the UpBrush, DownBrush, and Stroke.Brush are all transparent
       if (IsTransparent)
           Print("All bars are currently set to transparent");
   }
}
```
