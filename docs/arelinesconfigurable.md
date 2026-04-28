# AreLinesConfigurable

Source: https://developer.ninjatrader.com/docs/desktop/arelinesconfigurable

---

# AreLinesConfigurable


## [Definition](https://developer.ninjatrader.com/docs/desktop/arelinesconfigurable#definition)


Determines if the [line](https://developer.ninjatrader.com/docs/desktop/addline) used in an indicator are configurable from within the indicator dialog window.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/arelinesconfigurable#property-value)


A **bool** which true if any indicator line(s) are configurable; otherwise, false. Default set to true.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/arelinesconfigurable#syntax)


`AreLinesConfigurable`


## [Examples](https://developer.ninjatrader.com/docs/desktop/arelinesconfigurable#examples)
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Please note that in the following example, the indicator lines are not configurable.


```csharp
protected override void OnStateChange()
{
    if (State == State.SetDefaults)
    {
        AddLine(Brushes.Gray, 30, "Lower");
        AreLinesConfigurable = false; // Indicator lines are not configurable
    }
}
```
