# GetUnrealizedProfitLoss()

Source: https://developer.ninjatrader.com/docs/desktop/getunrealizedprofitloss

---

# GetUnrealizedProfitLoss()


## [Definition](https://developer.ninjatrader.com/docs/desktop/getunrealizedprofitloss#definition)


Calculates the unrealized PnL for the account position.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/getunrealizedprofitloss#method-return-value)


A **double** value representing the account's unrealized PnL.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/getunrealizedprofitloss#syntax)


`PositionAccount.GetUnrealizedProfitLoss(PerformanceUnit unit, [double price])`
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


- If no double argument is provided in the call, the current (real-time) Last price will be substituted in. In case Tools > Options > Trading > 'Use last price for Pnl' is unchecked or the instrument type is Forex / CFD the bid (for a long position) / ask (for a short position) would be used as a substitute.
- For back-testing a double price to compare against should be provided like in our example below.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/getunrealizedprofitloss#parameters)


| Parameter | Description |
| --- | --- |
| unit | Possible values: **PerformanceUnit.Currency** **PerformanceUnit.Percent** **PerformanceUnit.Pips** **PerformanceUnit.Points** **PerformanceUnit.Ticks** |
| price | Optional price passed in used to calculate the PnL such as **Close[0]**. This value is used as the current price and compared against your entry price for the PnL. |


## [Examples](https://developer.ninjatrader.com/docs/desktop/getunrealizedprofitloss#examples)


```csharp
protected override void OnBarUpdate()
{
    // If not flat print our unrealized PnL
    if (PositionAccount.MarketPosition != MarketPosition.Flat)
        Print("Open PnL: " + PositionAccount.GetUnrealizedProfitLoss(PerformanceUnit.Points, Close[0]));
}
```
