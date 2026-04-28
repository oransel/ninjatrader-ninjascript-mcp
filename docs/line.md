# Line

Source: https://developer.ninjatrader.com/docs/desktop/line

---

# Line


## [Definition](https://developer.ninjatrader.com/docs/desktop/line#definition)


Represents an interface that exposes information regarding a Line [IDrawingTool](https://developer.ninjatrader.com/docs/desktop/idrawingtool).


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/line#methods-and-properties)


| StartAnchor | An [IDrawingTool's ChartAnchor](https://developer.ninjatrader.com/docs/desktop/idrawingtool) representing the starting point of the drawing object |
| --- | --- |
| EndAnchor | An [IDrawingTool's ChartAnchor](https://developer.ninjatrader.com/docs/desktop/idrawingtool) representing the end point of the drawing object |
| Stroke | A [Stroke](https://developer.ninjatrader.com/docs/desktop/stroke_class) object used to draw the object |


## [Examples](https://developer.ninjatrader.com/docs/desktop/line#examples)


```csharp
// Instantiate a Line object
NinjaTrader.NinjaScript.DrawingTools.Line myLine = Draw.Line(this, "tag1", false, 10, 1000, 0, 1001, Brushes.LimeGreen, DashStyleHelper.Dot, 2);

// Set a new Stroke for the object
myLine.Stroke = new Stroke(Brushes.Green, DashStyleHelper.Dash, 5);
```

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


To differentiate between NinjaTrader.NinjaScript.DrawingTools.Line and NinjaTrader.Gui.Line when assigning a Line object, you will need to invoke the former path explicitly, as seen in the example above.
