# OnPositionUpdate()

Source: https://developer.ninjatrader.com/docs/desktop/onpositionupdate

---

# OnPositionUpdate()


## [Definition](https://developer.ninjatrader.com/docs/desktop/onpositionupdate#definition)


An event driven method which is called each time a PositionUpdate is received for the strategy.


- This method is typically called after [OnExecutionUpdate()](https://developer.ninjatrader.com/docs/desktop/onexecutionupdate).
- OnPositionUpdate() will update with PositionUpdates that are filtered for the strategy. The strategy [Position](https://developer.ninjatrader.com/docs/desktop/position) object is driven by Executions, and is updated as early as [OnExecutionUpdate()](https://developer.ninjatrader.com/docs/desktop/onexecutionupdate).
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


- You will NOT receive position updates for manually placed orders, or orders managed by other strategies (including any [ATM strategies](https://developer.ninjatrader.com/docs/desktop/using_atm_strategies)) in OnPositionUpdate(). The Account class contains a pre-built event handler ([PositionUpdate](https://developer.ninjatrader.com/docs/desktop/positionupdate)) which can be used to filter position updates on a specified account.
- It's best practice to only work with the passed by value parameters and not reference parameters. This insures that you process each change of the underlying state.
- Rithmic and Interactive Brokers Users: When using a NinjaScript strategy it is best practice to only work with passed by value data from OnExecution. Instances of multiple fills at the same time for the same instrument might result in an incorrect OnPositionUpdate, as sequence of events are not guaranteed due to provider API design. For an example on protecting positions with this approach, see [OnExecutionUpdate()](https://developer.ninjatrader.com/docs/desktop/onexecutionupdate).


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/onpositionupdate#method-return-value)


This method does not return a value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/onpositionupdate#syntax)


You must override the method in your strategy with the following syntax:


`protected override void OnPositionUpdate(Position position, double averagePrice, int quantity, MarketPosition marketPosition)`


## [Method Parameters](https://developer.ninjatrader.com/docs/desktop/onpositionupdate#method-parameters)


| Parameter | Description |
| --- | --- |
| position | A [Position](https://developer.ninjatrader.com/docs/desktop/position) object passed by reference representing the current position object |
| averageFillPrice | A double value representing the updating average fill price of a position |
| quantity | An int value representing the updating quantity of a position |
| marketPosition | A [MarketPosition](https://developer.ninjatrader.com/docs/desktop/marketposition) object representing the updating position update provided directly from the broker. This is not the actual Position core position object, but the last change of the market position |
| MarketPosition.Flat | MarketPosition.Long | MarketPosition.Short |


## [Examples](https://developer.ninjatrader.com/docs/desktop/onpositionupdate#examples)


```csharp
protected override void OnPositionUpdate(Cbi.Position position, double averagePrice,
      int quantity, Cbi.MarketPosition marketPosition)
{
  if (position.MarketPosition == MarketPosition.Flat)
  {
    // Do something like reset some variables here
  }
}
```


### Understanding the order object parameter vs updating value parameter ([Multi-Thread Considerations for NinjaScript](https://developer.ninjatrader.com/docs/desktop/multi_threading_consideration_for_ninjascript))


```csharp
protected override void OnPositionUpdate(Cbi.Position position, double averagePrice,
      int quantity, Cbi.MarketPosition marketPosition)
{
  Print("The most current MarketPosition is: " + position.MarketPosition);   // Flat
  Print("This particular position update marketPosition is: " + marketPosition); // Long
}
```


## [Additional Reference Samples](https://developer.ninjatrader.com/docs/desktop/onpositionupdate#additional-reference-samples)


Additional reference code samples are available in the [NinjaScript Educational Resources](https://developer.ninjatrader.com/docs/desktop/educational_resources) section.
