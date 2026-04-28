# BarBrushes

Source: https://developer.ninjatrader.com/docs/desktop/barbrushes

---

# BarBrushes


## [Definition](https://developer.ninjatrader.com/docs/desktop/barbrushes#definition)


A collection of historical brushes used for painting the color of a price bar's body.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/barbrushes#property-value)


A brush series type object. Accessing this property via an index value **int barsAgo** returns a **Brush** object representing the referenced bar's color.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This will only return the color of a bar in which an explicit color overwrite was used. Otherwise it will return null.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/barbrushes#syntax)


`BarBrushes`


`BarBrushes[int barsAgo]`
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


You may have up to 65,535 unique BarBrushes instances, therefore, using **static predefined brushes** should be favored. Alternatively, in order to use fewer brushes, please try to cache your custom brushes until a new brush would actually need to be created.


## [Examples](https://developer.ninjatrader.com/docs/desktop/barbrushes#examples)


```csharp
protected override void OnBarUpdate()
{
    if (CurrentBar < 1)
        return;

    // Sets the color of the current bar to blue.
    BarBrushes[0] = Brushes.Blue;

    // Sets the color of the previous bar to orange.
    BarBrushes[1] = Brushes.Orange;
}
```
