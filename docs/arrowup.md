# ArrowUp

Source: https://developer.ninjatrader.com/docs/desktop/arrowup

---

# ArrowUp


## [Definition](https://developer.ninjatrader.com/docs/desktop/arrowup#definition)


Represents an interface that exposes information regarding an Arrow Up [IDrawingTool](https://developer.ninjatrader.com/docs/desktop/idrawingtool).


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/arrowup#methods-and-properties)


| --- |
| Anchor | An [IDrawingTool](https://developer.ninjatrader.com/docs/desktop/idrawingtool)'s **ChartAnchor** representing the point of the drawing object |
| AreaBrush | A **Brush** object representing the fill color of the draw object |
| OutlineBrush | A **Brush** object representing the color of the draw object's outline |


## [Example](https://developer.ninjatrader.com/docs/desktop/arrowup#example)


```csharp
// Instantiate an ArrowDown object
ArrowUp myArrow = Draw.ArrowUp(this, "tag1", true, Time[0], Low[0] - (2 * TickSize), Brushes.Green);

// Set the outline color of the Arrow
myArrow.OutlineBrush = Brushes.Black;
```
