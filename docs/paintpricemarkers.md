# PaintPriceMarkers

Source: https://developer.ninjatrader.com/docs/desktop/paintpricemarkers

---

# PaintPriceMarkers


## [Definition](https://developer.ninjatrader.com/docs/desktop/paintpricemarkers#definition)


If true, any indicator plot values display price markers in the y-axis.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/paintpricemarkers#property-value)


This property returns true if the indicator plot values display in the y-axis; otherwise, false. Default set to true.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


Warning: This property should ONLY be set from the **OnStateChange()** method during **State.SetDefaults** or **State.Configure**.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/paintpricemarkers#syntax)


`PaintPriceMarkers`


## [Examples](https://developer.ninjatrader.com/docs/desktop/paintpricemarkers#examples)


```csharp
protected override void OnStateChange()
{
     if (State == State.SetDefaults)
     {
         PaintPriceMarkers = true; // Indicator plots values display in the y-axis
         AddPlot(Brushes.Orange, "SMA");
     }
}
```
