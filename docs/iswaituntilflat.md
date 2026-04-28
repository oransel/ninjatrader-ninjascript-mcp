# IsWaitUntilFlat

Source: https://developer.ninjatrader.com/docs/desktop/iswaituntilflat

---

# IsWaitUntilFlat


## [Definition](https://developer.ninjatrader.com/docs/desktop/iswaituntilflat#definition)


Indicates the strategy is currently waiting until a flat position is detected before submitting live orders.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This property would only apply if the strategy **StartBehavior** was set to **StartBehavior.WaitUntilFlat** or **StartBehavior.WaitUntilFlatSynchronizeAccount**.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/iswaituntilflat#property-value)


This property returns true if the strategy has detected it is either in a long or short position during **State.Transition**; otherwise false. Default value is set to false.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/iswaituntilflat#syntax)


`IsWaitUntilFlat`


## [Examples](https://developer.ninjatrader.com/docs/desktop/iswaituntilflat#examples)


```csharp
// If a strategy is waiting for a flat position, return and print a message
if (!IsWaitUntilFlat)
{
   Print("This strategy is currently waiting for a flat account position to begin placing trades");
   return;
}
```
