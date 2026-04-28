# GetAtmStrategyMarketPosition()

Source: https://developer.ninjatrader.com/docs/desktop/getatmstrategymarketposition

---

# GetAtmStrategyMarketPosition()


## [Definition](https://developer.ninjatrader.com/docs/desktop/getatmstrategymarketposition#definition)


Gets the current market position of the specified ATM Strategy.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Notes:


- Changes to positions will not be reflected till at least the next **OnBarUpdate()** event after an order fill.
- If the ATM Strategy does not exist then **MarketPosition.Flat** returns.
- Please note this provides access to the current ATM strategy position, which should not be confused with the NinjaScript strategy position or account position. For more information please see the [Using ATM Strategies](https://developer.ninjatrader.com/docs/desktop/using_atm_strategies) section.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/getatmstrategymarketposition#method-return-value)


- **MarketPosition.Flat**
- **MarketPosition.Long**
- **MarketPosition.Short**


## [Syntax](https://developer.ninjatrader.com/docs/desktop/getatmstrategymarketposition#syntax)


`GetAtmStrategyMarketPosition(string atmStrategyId)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/getatmstrategymarketposition#parameters)


| --- |
| **atmStrategyId** | The unique identifier for the ATM strategy |


## [Examples](https://developer.ninjatrader.com/docs/desktop/getatmstrategymarketposition#examples)


```csharp
protected override void OnBarUpdate()
{
    // Check if flat
    if (GetAtmStrategyMarketPosition("id") == MarketPosition.Flat)
        Print("ATM Strategy position is currently flat");
}
```
