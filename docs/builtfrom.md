# BuiltFrom

Source: https://developer.ninjatrader.com/docs/desktop/builtfrom

---

# BuiltFrom


## [Definition](https://developer.ninjatrader.com/docs/desktop/builtfrom#definition)


Determines the base dataset used to build the **BarsType** (i.e., Tick, Minute, Day). The **BuiltFrom** property will control the frequency in which [**OnDataPoint()**](https://developer.ninjatrader.com/docs/desktop/ondatapoint) processes historical data.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/builtfrom#property-value)


A [**BarsPeriodType**](https://developer.ninjatrader.com/docs/desktop/barsperiod) enum. Values that will be recognized include:


- **BarsPeriodType.Tick**
- **BarsPeriodType.Minute**
- **BarsPeriodType.Day**
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


Warning: Using other bars period types (e.g., Range, Volume, or other custom bars types) is NOT supported. The **BarsPeriodType** values mentioned above represent all of the fundamental data points needed to build a bar.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/builtfrom#syntax)


`BuiltFrom`


## [Examples](https://developer.ninjatrader.com/docs/desktop/builtfrom#examples)


```csharp
protected override void OnStateChange()
{
    if (State == State.SetDefaults)
    {
        Name     = "MyCustomBarsType";
        BarsPeriod   = new BarsPeriod { BarsPeriodType = (BarsPeriodType) 15, BarsPeriodTypeName = "MyCustomBarsType(15)", Value = 1 };
        BuiltFrom   = BarsPeriodType.Minute; // update OnDataPoint() every minute on historical data
        DaysToLoad   = 5;
    }

    else if (State == State.Configure)
    {
    }
}
```
