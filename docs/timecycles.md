# TimeCycles

Source: https://developer.ninjatrader.com/docs/desktop/timecycles

---

# TimeCycles


## [Definition](https://developer.ninjatrader.com/docs/desktop/timecycles#definition)


Represents an interface that exposes information regarding a TimeCycles **IDrawingTool**.


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/timecycles#methods-and-properties)


| Parameter | Description |
| --- | --- |
| Anchor | An **IDrawingTool's ChartAnchor** representing the point of the drawing object |
| OutlineStroke | A Stroke used for the outline of the region |
| AreaBrush | A **Brush** object representing the fill color of the draw object |


## [Examples](https://developer.ninjatrader.com/docs/desktop/timecycles#examples)


```csharp
// Instantiate a Time Cycles object
TimeCycles myTimeCycles = (this, "tag1", 0, 10, Brushes.CornflowerBlue, Brushes.CornflowerBlue, 40);

// Change the object's OutlineBrush
myTimeCycles.OutlineStroke = new Stroke(Brushes.Red);
```
