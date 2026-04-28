# DisconnectDelaySeconds

Source: https://developer.ninjatrader.com/docs/desktop/disconnectdelayseconds

---

# DisconnectDelaySeconds


## [Definition](https://developer.ninjatrader.com/docs/desktop/disconnectdelayseconds#definition)


Determines the amount of time a disconnect would have to last before **connection loss handling** takes action.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/disconnectdelayseconds#property-value)


An **int** value represents the time required for a disconnect to last before connection loss handling actions will occur. Default value is 10.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/disconnectdelayseconds#syntax)


`DisconnectDelaySeconds`


## [Examples](https://developer.ninjatrader.com/docs/desktop/disconnectdelayseconds#examples)


```csharp
protected override void OnStateChange()
{
     if (State == State.SetDefaults)
     {
         // Disconnect has to be at least 10 seconds
         DisconnectDelaySeconds = 10;
     }
}
```
