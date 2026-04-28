# PositionAccount

Source: https://developer.ninjatrader.com/docs/desktop/positionaccount

---

# PositionAccount


## [Definition](https://developer.ninjatrader.com/docs/desktop/positionaccount#definition)


Represents position related information that pertains to real-world account (live or simulation).
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Tips:


- For multi-instrument scripts, please see **PositionsAccount** object which holds an array of all instrument positions managed by the strategy's account.
- For a Strategy Position, please see **Position**.


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/positionaccount#methods-and-properties)


| Property | Description |
| --- | --- |
| **Account** | An **Account** object which corresponds to the position |
| **AveragePrice** | Gets the average entry price of the account position |
| **GetUnrealizedProfitLoss()** | Gets the unrealized PnL for the account |
| **Instrument** | An **Instrument** value representing the instrument of an order |
| **MarketPosition** | Gets the current market position of the account

- Possible values:

- **MarketPosition.Flat**
- **MarketPosition.Long**
- **MarketPosition.Short** |
| **Quantity** | Gets the current account position size |
| **ToString()** | A string representation of an account position |


## [Examples](https://developer.ninjatrader.com/docs/desktop/positionaccount#examples)


```csharp
protected override void OnBarUpdate()
{
    // Print out the average entry price
    Print("The average entry price is " + PositionAccount.AveragePrice);
}
```
