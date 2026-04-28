# GetAtmStrategyPositionQuantity()

Source: https://developer.ninjatrader.com/docs/desktop/getatmstrategypositionquantity

---

# GetAtmStrategyPositionQuantity()


## [Definition](https://developer.ninjatrader.com/docs/desktop/getatmstrategypositionquantity#definition)


Gets the current position quantity of the specified ATM Strategy.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Changes to positions will not be reflected till at least the next **OnBarUpdate()** event after an order fill.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/getatmstrategypositionquantity#method-return-value)


An **int** value representing the quantity.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/getatmstrategypositionquantity#syntax)


`GetAtmStrategyPositionQuantity(string atmStrategyId)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/getatmstrategypositionquantity#parameters)


| --- |
| **atmStrategyId** | The unique identifier for the ATM strategy |


## [Examples](https://developer.ninjatrader.com/docs/desktop/getatmstrategypositionquantity#examples)


```csharp
protected override void OnBarUpdate()
{
     // Check if flat
     if (GetAtmStrategyMarketPosition("idValue") != MarketPosition.Flat)
         Print("Position size is " + GetAtmStrategyPositionQuantity("idValue").ToString());
}
```
