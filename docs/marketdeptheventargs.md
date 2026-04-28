# MarketDepthEventArgs

Source: https://developer.ninjatrader.com/docs/desktop/marketdeptheventargs

---

# MarketDepthEventArgs


## [Definition](https://developer.ninjatrader.com/docs/desktop/marketdeptheventargs#definition)


Represents a change in level two market data also known as market depth and is passed as a parameter in the **OnMarketDepth()** method.


## [Methods and Parameters](https://developer.ninjatrader.com/docs/desktop/marketdeptheventargs#methods-and-parameters)


| Instrument | IsReset | MarketDataType | MarketMaker | Operation | Position | Price | Time | ToString() | Volume |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| A **Instrument** object representing the instrument of the market data | A bool value representing if a UI reset is needed after a manual disconnect.
Note: This is only relevant for columns. Whenever this property is true, the UI needs to be reset. | Possible values are:
**MarketDataType.Ask**
**MarketDataType.Bid** | A string representing the market maker id | Represents the action you should take when building a level two book.
Possible values are:
**Operation.Add**
**Operation.Update**
**Operation.Remove** | An **int** value representing the zero based position in the depth ladder. | A **double** value representing the price | A **DateTime** structure representing the time | A string representation of the **MarketDataEventArgs** object | A long value representing volume |


## [Examples](https://developer.ninjatrader.com/docs/desktop/marketdeptheventargs#examples)


```csharp
protected override void OnMarketDepth(MarketDepthEventArgs marketDepthUpdate)
{
     // Print some data to the Output window
     if (marketDepthUpdate.MarketDataType == MarketDataType.Ask && marketDepthUpdate.Operation == Operation.Update)
         Print("The most recent ask change is " + marketDepthUpdate.Price + " " + marketDepthUpdate.Volume);
}
```

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Tip: For an example of how to use **IsReset** please see \MarketAnalyzerColumns\AskPrice.cs
