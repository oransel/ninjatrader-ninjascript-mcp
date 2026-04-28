# IsChartOnly

Source: https://developer.ninjatrader.com/docs/desktop/ischartonly

---

# IsChartOnly


## [Definition](https://developer.ninjatrader.com/docs/desktop/ischartonly#definition)


If true, any indicator will be only available for charting usage - indicators with this property enabled would for example not be expected to show if called in a SuperDOM or MarketAnalyzer window.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/ischartonly#property-value)


This property returns true if the indicator can only be used on a chart; otherwise, false. Default set to false.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


This property should ONLY be set from the **OnStateChange()** method during **State.SetDefaults** or **State.Configure**.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/ischartonly#syntax)


`IsChartOnly`


## [Examples](https://developer.ninjatrader.com/docs/desktop/ischartonly#examples)


```csharp
protected override void OnStateChange()
{
    if (State == State.SetDefaults)
    {
        IsChartOnly = true; // Allow the indicator to work in charting environment only
    }
}
```
