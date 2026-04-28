# BackBrushesAll

Source: https://developer.ninjatrader.com/docs/desktop/backbrushesall

---

# BackBrushesAll


## [Definition](https://developer.ninjatrader.com/docs/desktop/backbrushesall#definition)


A collection of historical brushes used for the background colors for all chart panels.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/backbrushesall#property-value)


A brush series type object. Accessing this property via an index value `[int barsAgo]` returns a **Brush** object representing the color of the background color on the referenced bar for all chart panels.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/backbrushesall#syntax)


`BackBrushesAll`


`BackBrushesAll[int barsAgo]`
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


You may have up to 65,535 unique BackBrushAll instances, therefore, using **static predefined brushes** should be favored. Alternatively, in order to use fewer brushes, please try to cache your custom brushes until a new brush would actually need to be created.


## [Examples](https://developer.ninjatrader.com/docs/desktop/backbrushesall#examples)


```csharp
protected override void OnBarUpdate()
{
    if (CurrentBar < 1)
        return;

    // Sets the color of the background on the current bar as blue on all chart panels.
    BackBrushesAll[0] = Brushes.Blue;

    // Sets the color of the background on the previous bar as orange on all chart panels.
    BackBrushesAll[1] = Brushes.Orange;
}
```
