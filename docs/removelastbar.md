# RemoveLastBar()

Source: https://developer.ninjatrader.com/docs/desktop/removelastbar

---

# RemoveLastBar()


## [Definition](https://developer.ninjatrader.com/docs/desktop/removelastbar#definition)


Removes the last data point for the Bars Type. There may be cases where your custom bar type may need to amend the last values added on a bar that has already closed. Calling **RemoveLastBar()** will remove the last points for that bar type and allow you to call **AddBar()** with the updated values.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


- In order to use this method, the [**IsRemoveLastBarSupported**](https://developer.ninjatrader.com/docs/desktop/isremovelastbarsupported) method must be true.
- **RemoveLastBar()** CANNOT be used with [**TickReplay**](https://ninjatrader.com/support/helpGuides/nt8/?tick_replay.htm)


## [Syntax](https://developer.ninjatrader.com/docs/desktop/removelastbar#syntax)


`RemoveLastBar(Bars bars)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/removelastbar#parameters)


| Parameter | Description |
| --- | --- |
| **bars** | The Bars object of your bars type |


## [Examples](https://developer.ninjatrader.com/docs/desktop/removelastbar#examples)


```csharp
RemoveLastBar(bars);
```
