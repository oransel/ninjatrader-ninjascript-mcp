# AllowRemovalOfDrawObjects

Source: https://developer.ninjatrader.com/docs/desktop/allowremovalofdrawobjects

---

# AllowRemovalOfDrawObjects


## [Definition](https://developer.ninjatrader.com/docs/desktop/allowremovalofdrawobjects#definition)


Determines if programmatically drawn **DrawObjects** are allowed to remove manually from the chart


## [Property Value](https://developer.ninjatrader.com/docs/desktop/allowremovalofdrawobjects#property-value)


When set to true, the draw objects from the indicator or strategy can be deleted from the chart manually by a user. If false, draw objects from the indicator or strategy can only be removed from the chart if the script removes the drawing object, or the script is terminates. Default set to false.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/allowremovalofdrawobjects#syntax)


`AllowRemovalOfDrawObjects`


## [Examples](https://developer.ninjatrader.com/docs/desktop/allowremovalofdrawobjects#examples)


```csharp
protected override void OnStateChange()
{
     Add(new Plot(Brushes.Orange, "SMA"));
     AllowRemovalOfDrawObjects = true; // Draw objects can be removed separately from the script
}
```
