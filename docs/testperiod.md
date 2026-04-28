# TestPeriod

Source: https://developer.ninjatrader.com/docs/desktop/testperiod

---

# TestPeriod


## [Definition](https://developer.ninjatrader.com/docs/desktop/testperiod#definition)


Reserved for **Walk-Forward Optimization**, this property determines the number of days used for the "out of sample" backtest period for a given strategy. See also **OptimizationPeriod**.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This property should ONLY be called from the **OnStateChange()** method during State.SetDefaults.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/testperiod#property-value)


An **int** value representing the number of "out of sample" days used for walk-forward optimization; Default value is set to 28.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/testperiod#syntax)


`TestPeriod`


## [Examples](https://developer.ninjatrader.com/docs/desktop/testperiod#examples)


```csharp
protected override void OnStateChange()
{
    if (State == State.SetDefaults)
    {
        //set the default TestPeriod to 31 days for WFOs
        TestPeriod = 31;
    }
}
```
