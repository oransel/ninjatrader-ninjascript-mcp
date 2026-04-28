# TriangleUp

Source: https://developer.ninjatrader.com/docs/desktop/triangleup

---

# TriangleUp


## [Definition](https://developer.ninjatrader.com/docs/desktop/triangleup#definition)


Represents an interface that exposes information regarding a Triangle Up [IDrawingTool](https://developer.ninjatrader.com/docs/desktop/idrawingtool).


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/triangleup#methods-and-properties)


| Parameter | Description |
| --- | --- |
| Anchor | An [IDrawingTool's ChartAnchor](https://developer.ninjatrader.com/docs/desktop/chartanchor) representing the point of the drawing object |
| AreaBrush | A [Brush](http://msdn.microsoft.com/en-us/library/system.windows.media.brush(v=vs.110).aspx) class representing the fill color of the draw object |
| OutlineBrush | A [Brush](http://msdn.microsoft.com/en-us/library/system.windows.media.brush(v=vs.110).aspx) class representing the outline color of the draw object |


## [Examples](https://developer.ninjatrader.com/docs/desktop/triangleup#examples)


```csharp
// Instantiate a TriangleUp object
TriangleUp myTri = Draw.TriangleUp(this, "tag1", true, 0, Low[0] - TickSize, Brushes.Red);

// Change the object's AreaBrush
myTri.AreaBrush = Brushes.Beige;
```
