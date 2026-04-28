# TriangleDown

Source: https://developer.ninjatrader.com/docs/desktop/triangledown

---

# TriangleDown


## [Definition](https://developer.ninjatrader.com/docs/desktop/triangledown#definition)


Represents an interface that exposes information regarding a Triangle Down [IDrawingTool](https://developer.ninjatrader.com/docs/desktop/idrawingtool).


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/triangledown#methods-and-properties)


| Parameter | Description |
| --- | --- |
| Anchor | An [IDrawingTool's ChartAnchor](https://developer.ninjatrader.com/docs/desktop/chartanchor) representing the point of the drawing object |
| AreaBrush | A [Brush](http://msdn.microsoft.com/en-us/library/system.windows.media.brush(v=vs.110).aspx) class representing the fill color of the draw object |
| OutlineBrush | A [Brush](http://msdn.microsoft.com/en-us/library/system.windows.media.brush(v=vs.110).aspx) class representing the outline color of the draw object |


## [Example](https://developer.ninjatrader.com/docs/desktop/triangledown#example)


```csharp
// Instantiate a TriangleDown object
TriangleDown myTri = Draw.TriangleDown(this, "tag1", true, 0, Low[0] - TickSize, Brushes.Red);

// Change the object's AreaBrush
myTri.AreaBrush = Brushes.Beige;
```
