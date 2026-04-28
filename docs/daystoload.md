# DaysToLoad

Source: https://developer.ninjatrader.com/docs/desktop/daystoload

---

# DaysToLoad


## [Definition](https://developer.ninjatrader.com/docs/desktop/daystoload#definition)


Determines the number of trading days which will be configured when loading the strategy from the Strategies Grid.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


- This property does NOT affect a strategy configured of a Chart or the Strategy Analyzer.
- A trading day is defined by a **Trading Hour** template


## [Property Value](https://developer.ninjatrader.com/docs/desktop/daystoload#property-value)


An **int** value determining the number of trading days to load for historical data processing. Default value is 5, but can be configured and overridden from the UI.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/daystoload#syntax)


`DaysToLoad`


## [Examples](https://developer.ninjatrader.com/docs/desktop/daystoload#examples)


```csharp
protected override void OnStateChange()
{
     if (State == State.SetDefaults)
     {
         DaysToLoad = 15;
     }
}
```
