# Position

Source: https://developer.ninjatrader.com/docs/desktop/position

---

# Position


## [Definition](https://developer.ninjatrader.com/docs/desktop/position#definition)


Represents position related information that pertains to an instance of a strategy.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Tips:


- For multi-instrument scripts, please see **Positions** object which holds an array of all instrument positions managed by the strategy's account.
- For a real-world Account Position, please see **PositionAccount**.


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/position#methods-and-properties)


| Property | Description |
| --- | --- |
| **Account** | An **Account** object which corresponds to the position |
| **AveragePrice** | Gets the average entry price of the strategy position |
| **GetUnrealizedProfitLoss()** | Gets the unrealized PnL |
| **Instrument** | An **Instrument** value representing the instrument of an order |
| **MarketPosition** | Gets the current market position

- Possible values:

- **MarketPosition.Flat**
- **MarketPosition.Long**
- **MarketPosition.Short** |
| **Quantity** | Gets the current position size |
| **ToString()** | A string representation of a position |


## [Examples](https://developer.ninjatrader.com/docs/desktop/position#examples)


```csharp
protected override void OnBarUpdate()
{
     // Print out the average entry price
     Print("The average entry price is " + Position.AveragePrice);
}
```
