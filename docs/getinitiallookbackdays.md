# GetInitialLookBackDays()

Source: https://developer.ninjatrader.com/docs/desktop/getinitiallookbackdays

---

# GetInitialLookBackDays()


## [Definition](https://developer.ninjatrader.com/docs/desktop/getinitiallookbackdays#definition)


Determines how many days of data load when a user makes a "bars back" data request.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/getinitiallookbackdays#method-return-value)


This method returns An **int** value.


## [Method Parameters](https://developer.ninjatrader.com/docs/desktop/getinitiallookbackdays#method-parameters)


| --- |
| **barsPeriod** | The [bars period](https://developer.ninjatrader.com/docs/desktop/barsperiod) chosen by the user when utilizing this Bars type |
| **tradingHours** | The [trading hours](https://developer.ninjatrader.com/docs/desktop/tradinghours) chosen by the user when utilizing this Bars type |
| **barsBack** | The bars back chosen by the user when utilizing this Bars type |


## [Syntax](https://developer.ninjatrader.com/docs/desktop/getinitiallookbackdays#syntax)


You must override the method in your Bars Type with the following syntax.


`public override int GetInitialLookBackDays(BarsPeriod barsPeriod, TradingHours tradingHours, int barsBack) { }`


## [Examples](https://developer.ninjatrader.com/docs/desktop/getinitiallookbackdays#examples)


```csharp
public override int GetInitialLookBackDays(BarsPeriod barsPeriod, TradingHours tradingHours, int barsBack)
{
     // Returns the minimum number of days needed to successfully load the number
     // of bars back requested for a monthly Bars type
     return (int) barsPeriod.Value * barsBack * 31;
}
```

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Tip: Try to request an amount of data that is just right for what is needed. Requesting too large a data set will result in unnecessary data being loaded. Requesting too small a data set will result in multiple requests being done.
