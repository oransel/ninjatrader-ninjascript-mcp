# ArrowLine

Source: https://developer.ninjatrader.com/docs/desktop/arrowline

---

# ArrowLine


## [Definition](https://developer.ninjatrader.com/docs/desktop/arrowline#definition)


Represents an interface that exposes information regarding an Arrow Line **IDrawingTool**.


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/arrowline#methods-and-properties)


| --- |
| StartAnchor | An **IDrawingTool's ChartAnchor** representing the starting point of the drawing object |
| EndAnchor | An **IDrawingTool's ChartAnchor** representing the end point of the drawing object |
| Stroke | A **Stroke** object used to draw the object |


## [Example](https://developer.ninjatrader.com/docs/desktop/arrowline#example)


```csharp
// Draw an ArrowLine object
ArrowLine myArrow = Draw.ArrowLine(this, "myArrowLine", 3, High[3], 1, High[1], Brushes.Blue, DashStyleHelper.DashDot, 3);

// Disable the arrow's visibility
myArrow.IsVisible = false;
```
