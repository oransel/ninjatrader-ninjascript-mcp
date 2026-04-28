# CleanUp()

Source: https://developer.ninjatrader.com/docs/desktop/cleanup

---

# CleanUp()


## [Definition](https://developer.ninjatrader.com/docs/desktop/cleanup#definition)


Unregisters LinkControls (**IInstrumentProvider**) and calls **Cleanup()** on **ICleanable** controls on the **NTTabPage**. Override this to, e.g., unsubscribe from events or perform any other cleanup operations when the tab is closed.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


When overriding **Cleanup()**, it is strongly recommended when you call **base.Cleanup()** which ensures any link controls are also unregistered. The base implementation will also handle cleaning up any controls which implement **ICleanable**: **AccountSelector**, **AtmStrategySelector**, **InstrumentSelector**, **IntervalSelector**, **TifSelector**.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/cleanup#method-return-value)


This method does not return a value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/cleanup#syntax)


`public override void Cleanup()`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/cleanup#parameters)


This method does not accept any parameters.


## [Examples](https://developer.ninjatrader.com/docs/desktop/cleanup#examples)


```csharp
public override void Cleanup()
{
    // unregister from any custom events
    Connection.ConnectionStatusUpdate -= OnConnectionStatusUpdate;

    // a call to base.Cleanup() will loop through the visual tree looking for all ICleanable children
    // i.e., AccountSelector, AtmStrategySelector, InstrumentSelector, IntervalSelector, TifSelector,
    // as well as unregister any link control events

    base.Cleanup();
}
```
