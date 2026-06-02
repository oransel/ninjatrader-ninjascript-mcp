# AverageMfe

Source: https://developer.ninjatrader.com/docs/desktop/averagemfe

---

# AverageMfe


## [Definition](https://developer.ninjatrader.com/docs/desktop/averagemfe#definition)


Returns the average MFE (max favorable excursion) of the collection.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/averagemfe#property-value)


A **double** value that represents the average MFE of the collection.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/averagemfe#syntax)


`TradeCollection.TradesPerformance.TradesPerformanceValues.AverageMfe`


## [Examples](https://developer.ninjatrader.com/docs/desktop/averagemfe#examples)
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


The following example prints out the average MFE of all trades in currency.


```csharp
protected override void OnBarUpdate()
{
     // Print out the average MFE of all trades in currency
     Print("Average MFE of all trades is: " + SystemPerformance.AllTrades.TradesPerformance.Currency.AverageMfe);
}
```
