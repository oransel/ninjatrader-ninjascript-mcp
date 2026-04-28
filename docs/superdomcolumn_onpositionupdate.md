# OnPositionUpdate()

Source: https://developer.ninjatrader.com/docs/desktop/superdomcolumn_onpositionupdate

---

# OnPositionUpdate()


## [Definition](https://developer.ninjatrader.com/docs/desktop/superdomcolumn_onpositionupdate#definition)


Called every time a position changes state.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


The OnPositionUpdate() method is called on ALL position updates (e.g., any account and instrument combination) and NOT just the specific items which are selected in the SuperDOM.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/superdomcolumn_onpositionupdate#method-return-value)


This method does not return a value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/superdomcolumn_onpositionupdate#syntax)


`protected override void OnPositionUpdate(PositionEventArgs positionUpdate)`


## [Method Parameters](https://developer.ninjatrader.com/docs/desktop/superdomcolumn_onpositionupdate#method-parameters)


| Parameter | Description |
| --- | --- |
| **positionUpdate** | A **PositionEventArgs** representing the change in position |


## [Examples](https://developer.ninjatrader.com/docs/desktop/superdomcolumn_onpositionupdate#examples)


```csharp
protected override void OnPositionUpdate(PositionEventArgs positionUpdate)
{
  // Do not take action if the position update does not come from the selected SuperDOM instrument/account
  if (positionUpdate.Position.Instrument != SuperDom.Instrument
    || positionUpdate.Position.Account != SuperDom.Account)
    return;

  // Do something
}
```
