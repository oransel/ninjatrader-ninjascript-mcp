# Triangle

Source: https://developer.ninjatrader.com/docs/desktop/triangle

---

# Triangle


## [Definition](https://developer.ninjatrader.com/docs/desktop/triangle#definition)


Represents an interface that exposes information regarding a Triangle [IDrawingTool](https://developer.ninjatrader.com/docs/desktop/idrawingtool).


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/triangle#methods-and-properties)


| Parameter | Description |
| --- | --- |
| StartAnchor | An [IDrawingTool's ChartAnchor](https://developer.ninjatrader.com/docs/desktop/chartanchor) representing the starting point of the drawing object |
| MiddleAnchor | An [IDrawingTool's ChartAnchor](https://developer.ninjatrader.com/docs/desktop/chartanchor) representing the middle point of the drawing object |
| EndAnchor | An [IDrawingTool's ChartAnchor](https://developer.ninjatrader.com/docs/desktop/chartanchor) representing the end point of the drawing object |
| AreaBrush | A [Brush](http://msdn.microsoft.com/en-us/library/system.windows.media.brush(v=vs.110).aspx) class representing the fill color of the draw object |
| AreaOpacity | An int value representing the opacity of the area color |
| OutlineStroke | The [Stroke](https://developer.ninjatrader.com/docs/desktop/stroke_class) object used to draw the object's outline |


## [Example](https://developer.ninjatrader.com/docs/desktop/triangle#example)


```csharp
// Instantiate a Triangle object
Triangle myTri = Draw.Triangle(this, "tag1", 4, Low[4], 3, High[3], 1, Low[1], Brushes.Blue);

// Change the object's AreaOpacity
myTri.AreaOpacity = 100;
```
