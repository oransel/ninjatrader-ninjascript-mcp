# DisplayInDataBox

Source: https://developer.ninjatrader.com/docs/desktop/displayindatabox

---

# DisplayInDataBox


## [Definition](https://developer.ninjatrader.com/docs/desktop/displayindatabox#definition)


Determines if plot(s) display in the chart data box.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/displayindatabox#property-value)


This property returns true if the indicator plot(s) values display in the chart data box; otherwise, false. Default set to true.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


This property should ONLY be set from the **OnStateChange()** method during **State.SetDefaults** or **State.Configure**.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/displayindatabox#syntax)


`DisplayInDataBox`


## [Examples](https://developer.ninjatrader.com/docs/desktop/displayindatabox#examples)


```csharp
protected override void OnStateChange()
{
    if (State == State.SetDefaults)
    {
        DisplayInDataBox = false;
        AddPlot(Brushes.Orange, "SMA");
    }
}
```
