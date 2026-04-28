# PointValue

Source: https://developer.ninjatrader.com/docs/desktop/pointvalue

---

# PointValue


## [Definition](https://developer.ninjatrader.com/docs/desktop/pointvalue#definition)


Indicates the currency value of 1 full point of movement. For example, 1 point in the **S&P 500 Emini** futures contract (ES) is $50 USD which is equal to $12.50 USD per tick.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/pointvalue#property-value)


A **double** value representing the currency value of 1 point of movement.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/pointvalue#syntax)


`Instrument.MasterInstrument.PointValue`


## [Examples](https://developer.ninjatrader.com/docs/desktop/pointvalue#examples)


```csharp
// protected override void OnBarUpdate()
{
    // Displays the master instrument's point value at the bottom right of the chart
    Draw.TextFixed(this, "Point value: ", Bars.Instrument.MasterInstrument.PointValue.ToString(), TextPosition.BottomRight);
}
```


## [Additional Access Information](https://developer.ninjatrader.com/docs/desktop/pointvalue#additional-access-information)


This property can be accessed without a null reference check in the **OnBarUpdate()** event handler. When the **OnBarUpdate()** event is triggered, there will always be an **Instrument** object. Should you wish to access this property elsewhere, check for null reference first. e.g. if (**Instrument** != null)
