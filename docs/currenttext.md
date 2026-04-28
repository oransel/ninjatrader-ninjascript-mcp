# CurrentText

Source: https://developer.ninjatrader.com/docs/desktop/currenttext

---

# CurrentText


## [Definition](https://developer.ninjatrader.com/docs/desktop/currenttext#definition)


Sets text to be displayed in the Market Analyzer column.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


**CurrentText** will overrule any value set for [**CurrentValue**](https://developer.ninjatrader.com/docs/desktop/currentvalue). If both **CurrentValue** and **CurrentText** have assigned values, the value of **CurrentText** will display in the column.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/currenttext#property-value)


A string representing text to display in the column.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/currenttext#syntax)


`CurrentText`


## [Examples](https://developer.ninjatrader.com/docs/desktop/currenttext#examples)


```csharp
protected override void OnMarketData(MarketDataEventArgs marketDataUpdate)
{
   // Print "Ask" in the column if an Ask price update is received
   if(marketDataUpdate.MarketDataType == MarketDataType.Ask)
       CurrentText = "Ask";
}
```
