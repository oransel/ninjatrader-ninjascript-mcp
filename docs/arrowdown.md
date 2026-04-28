# ArrowDown

Source: https://developer.ninjatrader.com/docs/desktop/arrowdown

---

# ArrowDown


## [Definition](https://developer.ninjatrader.com/docs/desktop/arrowdown#definition)


Represents an interface that exposes information regarding an Arrow Down IDrawingTool.


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/arrowdown#methods-and-properties)


| Anchor | An IDrawingTool's ChartAnchor representing the point of the drawing object |
| --- | --- |
| AreaBrush | A Brush object representing the fill color of the draw object |
| OutlineBrush | A Brush object representing the color of the draw object's outline |


## [Example](https://developer.ninjatrader.com/docs/desktop/arrowdown#example)


```csharp
// Instantiate an ArrowDown object
ArrowDown myArrow = Draw.ArrowDown(this, "tag1", true, Time[0], High[0] + (2 * TickSize), Brushes.Green);

// Set the outline color of the Arrow
myArrow.OutlineBrush = Brushes.Black;
```
