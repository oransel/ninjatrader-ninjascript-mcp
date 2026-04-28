# VerticalLine

Source: https://developer.ninjatrader.com/docs/desktop/verticalline

---

# VerticalLine


## [Definition](https://developer.ninjatrader.com/docs/desktop/verticalline#definition)


Represents an interface that exposes information regarding a Vertical Line [IDrawingTool](https://developer.ninjatrader.com/docs/desktop/idrawingtool).


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/verticalline#methods-and-properties)


| Parameter | Description |
| --- | --- |
| StartAnchor | An [IDrawingTool's ChartAnchor](https://developer.ninjatrader.com/docs/desktop/chartanchor) representing the starting point of the drawing object |
| EndAnchor | An [IDrawingTool's ChartAnchor](https://developer.ninjatrader.com/docs/desktop/chartanchor) representing the end point of the drawing object |
| Stroke | A [Stroke](https://developer.ninjatrader.com/docs/desktop/stroke_class) object used to draw the object |


## [Examples](https://developer.ninjatrader.com/docs/desktop/verticalline#examples)


```csharp
// Instantiate a VerticalLine object
VerticalLine myLine = Draw.VerticalLine(this, "tag1", 10, Brushes.Black);

// Change the object's Stroke
myLine.Stroke = new Stroke(Brushes.BlanchedAlmond, DashStyleHelper.Dot, 5);
```
