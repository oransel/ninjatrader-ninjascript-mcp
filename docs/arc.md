# Arc

Source: https://developer.ninjatrader.com/docs/desktop/arc

---

# Arc


## [Definition](https://developer.ninjatrader.com/docs/desktop/arc#definition)


Represents an interface that exposes information regarding an Arc **IDrawingTool**.


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/arc#methods-and-properties)


| Parameter | Description |
| --- | --- |
| StartAnchor | An IDrawingTool's ChartAnchor representing the starting point of the drawing object |
| EndAnchor | An IDrawingTool's ChartAnchor representing the end point of the drawing object |
| AreaBrush | A Brush object representing the fill color of the draw object |
| AreaOpacity | An int value representing the opacity of the area color |
| ArcStroke | The Stroke object used to draw the arc line of the object's outline |
| Stroke | The Stroke object used to draw the straight line of the object's outline |


## [Example](https://developer.ninjatrader.com/docs/desktop/arc#example)


```csharp
// Draw an Arc object
Arc myArc = Draw.Arc(this, "myArc", Time[10], Close[10], Time[0], Close[0], Brushes.Blue);

// Set the opacity of the shading between the arc and the chord
myArc.AreaOpacity = 100;
```
