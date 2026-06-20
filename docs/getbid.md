# GetBid()

Source: https://developer.ninjatrader.com/docs/desktop/getbid

---

# GetBid()


## [Definition](https://developer.ninjatrader.com/docs/desktop/getbid#definition)


Returns the bid price value at a selected absolute bar index value.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


- This method does NOT return the current real-time bid price, but rather the historical / real-time bid price at the desired index. For obtaining the current real-time bid price, please use **GetCurrentBid()**.
- This method returns expected values when 1 tick bid / ask stamped data is used and available from **your provider**.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/getbid#method-return-value)


A **double** value that represents the bidding price at the desired bar index.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/getbid#syntax)


`Bars.GetBid(int index)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/getbid#parameters)


| Parameter | Description |
| --- | --- |
| **index** | The absolute bar index value used |


## [Examples](https://developer.ninjatrader.com/docs/desktop/getbid#examples)


```csharp
protected override void OnBarUpdate()
{
   // If the Highs of the two most recent bars are falling, place a long stop market order
   // at the Ask price
   if (Low[0] > Low[1] && Low[1] < Low[2])
   {
     EnterShortStopMarket(Bars.GetBid(CurrentBar));
   }
}
```
