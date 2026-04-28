# DownBrush

Source: https://developer.ninjatrader.com/docs/desktop/downbrush

---

# DownBrush


## [Definition](https://developer.ninjatrader.com/docs/desktop/downbrush#definition)


A **Brush** object used to determine the color to paint the down bars for the ChartStyle.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This Windows Presentation Forms (WPF) implementation of the Brush class is not directly used to paint bars on the chart. Instead it is converted to a SharpDX Brush in the **DownBrushDX** property. This property is used to capture user input for changing brush colors.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/downbrush#property-value)


A **WPF** Brush object used to paint the down bars.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/downbrush#syntax)


`DownBrush`


## [Examples](https://developer.ninjatrader.com/docs/desktop/downbrush#examples)


```csharp
protected override void OnStateChange()
{
    if (State == State.Configure)
    {
        // Set a new name for the DownBrush property
        SetPropertyName("DownBrush", "DecliningBrush");
    }
}
```
