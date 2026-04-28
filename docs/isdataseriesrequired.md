# IsDataSeriesRequired

Source: https://developer.ninjatrader.com/docs/desktop/isdataseriesrequired

---

# IsDataSeriesRequired


## [Definition](https://developer.ninjatrader.com/docs/desktop/isdataseriesrequired#definition)


Determines if a Data Series is required for calculating this **NinjaScript** object. When set to false, data series related properties will not be displayed on the UI when configuring.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


When set to false, methods and properties which are dependent on Bars will NOT be used. This means you will not receive any calls to **OnBarUpdate()** or be able to access historical bar prices.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/isdataseriesrequired#property-value)


This property returns true if the **NinjaScript** requires a Data Series; otherwise, false. Default value is true.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


Warning: This property should ONLY be set from the **OnStateChange()** method during **State.SetDefaults** or **State.Configure**.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/isdataseriesrequired#syntax)


`IsDataSeriesRequired`


## [Examples](https://developer.ninjatrader.com/docs/desktop/isdataseriesrequired#examples)


```csharp
protected override void OnStateChange()
{
    if (State == State.SetDefaults)
    {
        IsDataSeriesRequired = false;
    }
}
```
