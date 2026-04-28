# DrawVerticalGridLines

Source: https://developer.ninjatrader.com/docs/desktop/drawverticalgridlines

---

# DrawVerticalGridLines


## [Definition](https://developer.ninjatrader.com/docs/desktop/drawverticalgridlines#definition)


Plots vertical grid lines on the indicator panel.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


The indicator panel's parent chart has a similar option 'Grid line - vertical' which if Visible property set to false, will override the indicator's local setting if true.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/drawverticalgridlines#property-value)


This property returns true if vertical grid lines are plotted on the indicator panel; otherwise, false. Default set to true.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


This property should ONLY be set from the **OnStateChange()** method during State.SetDefaults or State.Configure.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/drawverticalgridlines#syntax)


`DrawVerticalGridLines`


## [Examples](https://developer.ninjatrader.com/docs/desktop/drawverticalgridlines#examples)


```csharp
protected override void OnStateChange()
{
     if (State == State.SetDefaults)
     {
         DrawVerticalGridLines = false; // Vertical grid lines will not plot on the indicator panel
         AddPlot(Brushes.Orange, "SMA");
     }
}
```
