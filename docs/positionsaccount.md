# PositionsAccount

Source: https://developer.ninjatrader.com/docs/desktop/positionsaccount

---

# PositionsAccount


## [Definition](https://developer.ninjatrader.com/docs/desktop/positionsaccount#definition)


Holds an array of **PositionAccount** objects that represent positions managed by the strategy's account. This property should only be used when your strategy is executing orders against **multiple instruments**.


Index value is based on the array of Bars objects added via the **AddDataSeries()** method. For example:


First Bars is ES 1 Minute
Secondary Bars is ES 5 Minute
Third Bars is NQ 5 Minute


**PositionsAccount[0]** == ES position
**PositionsAccount[1]** == Always a flat position, ES position will always be **PositionsAccount[0]**
**PositionsAccount[2]** == NQ position
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Tips:


- For single instrument scripts, please see **PositionAccount** object
- For Strategy Positions, please see **Positions**


## [Property Value](https://developer.ninjatrader.com/docs/desktop/positionsaccount#property-value)


An array of **PositionAccount** objects.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/positionsaccount#syntax)


`PositionsAccount[int index]`


## [Examples](https://developer.ninjatrader.com/docs/desktop/positionsaccount#examples)


```csharp
protected override void OnStateChange()
{
   if (State == State.SetDefaults)
   {
     Name = "ExampleStrategy";

   }

   else if (State == State.Configure)
   {
     AddDataSeries("ES 03-15", BarsPeriodType.Minute, 5);
     AddDataSeries("NQ 03-15", BarsPeriodType.Minute, 5);
   }
}

protected override void OnBarUpdate()
{
     Print("ES account position is " + PositionsAccount[0].MarketPosition);
     Print("NQ account position is " + PositionsAccount[2].MarketPosition);

     // Alternative approach. By checking what Bars object is calling the OnBarUpdate()
     // method, we can just use the Position property since its pointing to the correct
     // position.
     if (BarsInProgress == 0)
         Print("ES account position is " + PositionAccount.MarketPosition);
     else if (BarsInProgress == 2)
         Print("NQ account position is " + PositionAccount.MarketPosition);
}
```
