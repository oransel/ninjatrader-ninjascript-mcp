# OptimizationPeriod

Source: https://developer.ninjatrader.com/docs/desktop/optimizationperiod

---

# OptimizationPeriod


## [Definition](https://developer.ninjatrader.com/docs/desktop/optimizationperiod#definition)


Reserved for **Walk-Forward Optimization**, this property determines the number of days used for the "in sample" backtest period for a given strategy. See also **TestPeriod**.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This property should ONLY be called from the **OnStateChange()** method during State.SetDefaults.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/optimizationperiod#property-value)


An **int** value representing the number of "in sample" days used for walk-forward optimization; Default value is set to 10.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/optimizationperiod#syntax)


`OptimizationPeriod`


## [Examples](https://developer.ninjatrader.com/docs/desktop/optimizationperiod#examples)


```csharp
protected override void OnStateChange()
{
    if (State == State.SetDefaults)
    {
        //set the default optimization period to 20 days for WFOs
        OptimizationPeriod = 20;
    }
}
```
