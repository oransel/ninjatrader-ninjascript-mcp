# Square

Source: https://developer.ninjatrader.com/docs/desktop/square

---

# Square


## [Definition](https://developer.ninjatrader.com/docs/desktop/square#definition)


Represents an interface that exposes information regarding a Square **IDrawingTool**.


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/square#methods-and-properties)


| Parameter | Description |
| --- | --- |
| Anchor | An **IDrawingTool's ChartAnchor** representing the point of the drawing object |
| OutlineBrush | A **Brush** used for the outline of the square |
| AreaBrush | A **Brush** object representing the fill color of the draw object |


## [Examples](https://developer.ninjatrader.com/docs/desktop/square#examples)


```csharp
// Instantiate a Square object
Square mySquare = Draw.Square(this, "tag1", true, 0, Low[0] - TickSize, Brushes.Red);

// Change the object's OutlineBrush
mySquare.OutlineBrush = Brushes.Blue;
```
