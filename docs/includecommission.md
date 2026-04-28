# IncludeCommission

Source: https://developer.ninjatrader.com/docs/desktop/includecommission

---

# IncludeCommission


## [Definition](https://developer.ninjatrader.com/docs/desktop/includecommission#definition)


Determines if the strategy performance results will include commission on a historical backtest. When true, the **Commission Template** applied to the account on which the strategy is running will be used.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/includecommission#property-value)


A bool value which returns true if the strategy includes commission on a historical backtest; otherwise, false. Default value is set to false.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


This property should ONLY be set from the **OnStateChange()** method during **State.SetDefaults** or **State.Configure**.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/includecommission#syntax)


`IncludeCommission`


## [Examples](https://developer.ninjatrader.com/docs/desktop/includecommission#examples)


```csharp
protected override void OnStateChange()
{
    if (State == State.SetDefaults)
    {
        IncludeCommission = true;
    }
}
```
