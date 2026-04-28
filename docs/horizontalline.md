# HorizontalLine

Source: https://developer.ninjatrader.com/docs/desktop/horizontalline

---

# HorizontalLine


## [Definition](https://developer.ninjatrader.com/docs/desktop/horizontalline#definition)


Represents an interface that exposes information regarding a Horizontal Line **IDrawingTool**.


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/horizontalline#methods-and-properties)


| --- |
| StartAnchor | An **IDrawingTool's ChartAnchor** representing the starting point of the drawing object |
| Stroke | A **Stroke** object used to draw the object |


## [Examples](https://developer.ninjatrader.com/docs/desktop/horizontalline#examples)


```csharp
// Instantiate a HorizontalLine object
HorizontalLine myLine = Draw.HorizontalLine(this, "tag1", 1000, Brushes.Black);

// Set a new Stroke for the object
myLine.Stroke = new Stroke(Brushes.Green, DashStyleHelper.Dash, 5);
```
