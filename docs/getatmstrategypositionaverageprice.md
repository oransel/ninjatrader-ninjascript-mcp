# GetAtmStrategyPositionAveragePrice()

Source: https://developer.ninjatrader.com/docs/desktop/getatmstrategypositionaverageprice

---

# GetAtmStrategyPositionAveragePrice()


## [Definition](https://developer.ninjatrader.com/docs/desktop/getatmstrategypositionaverageprice#definition)


Gets the current position's average price of the specified ATM Strategy.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Changes to positions will not be reflected till at least the next **OnBarUpdate()** event after an order fill.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/getatmstrategypositionaverageprice#method-return-value)


A **double** value representing the average price.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/getatmstrategypositionaverageprice#syntax)


`GetAtmStrategyPositionAveragePrice(string atmStrategyId)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/getatmstrategypositionaverageprice#parameters)


| --- |
| **atmStrategyId** | The unique identifier for the ATM strategy |


## [Examples](https://developer.ninjatrader.com/docs/desktop/getatmstrategypositionaverageprice#examples)


```csharp
protected override void OnBarUpdate()
{
     // Check if flat
     if (GetAtmStrategyMarketPosition("id") != MarketPosition.Flat)
         Print("Average price is " + GetAtmStrategyPositionAveragePrice("id").ToString());
}
```
