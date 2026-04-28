# PositionUpdate

Source: https://developer.ninjatrader.com/docs/desktop/positionupdate

---

# PositionUpdate


## [Definition](https://developer.ninjatrader.com/docs/desktop/positionupdate#definition)


**PositionUpdate** can be used for subscribing to position update events.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Remember to unsubscribe if you are no longer using the subscription.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/positionupdate#syntax)


`PositionUpdate`


## [Examples](https://developer.ninjatrader.com/docs/desktop/positionupdate#examples)


```csharp
/*Example of subscribing/unsubscribing to position update events from an Add On. The concept can be carried over to any NinjaScript object you may be working on.*/
public class MyAddOnTab : NTTabPage
{
     private Account account;
     public MyAddOnTab()
     {
         // Find our Sim101 account
         lock (Account.All)
               account = Account.All.FirstOrDefault(a => a.Name == "Sim101");

         // Subscribe to position updates
         if (account != null)
               account.PositionUpdate += OnPositionUpdate;
     }

     // This method is fired as a position changes
     private void OnPositionUpdate(object sender, PositionEventArgs e)
     {
         // Output the new position
         NinjaTrader.Code.Output.Process(string.Format("Instrument: {0} MarketPosition: {1} AveragePrice: {2} Quantity: {3}",
               e.Position.Instrument.FullName, e.MarketPosition, e.AveragePrice, e.Quantity), PrintTo.OutputTab1);
     }

     // Called by TabControl when tab is being removed or window is closed
     public override void Cleanup()
     {
         // Make sure to unsubscribe to the positions subscription
         if (account != null)
               account.PositionUpdate -= OnPositionUpdate;
     }

     // Other required NTTabPage members left out for demonstration purposes. Be sure to add them in your own code.
}
```

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


The core MarketPosition e.Position is considered flat when Operation.Remove is seen, thus any related tracking in your logic you want to trigger or update should be aware. An Operation.Update would be seen if there was no flat state in between, i.e. on a reverse of the position.
