# Region

Source: https://developer.ninjatrader.com/docs/desktop/region

---

# Region


## [Definition](https://developer.ninjatrader.com/docs/desktop/region#definition)


Represents an interface that exposes information regarding a **Region** [IDrawingTool](https://developer.ninjatrader.com/docs/desktop/idrawingtool).


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/region#methods-and-properties)


| Parameter | Description |
| --- | --- |
| StartAnchor | An [IDrawingTool's ChartAnchor](https://developer.ninjatrader.com/docs/desktop/chartanchor) representing the starting point of the drawing object |
| EndAnchor | An [IDrawingTool's ChartAnchor](https://developer.ninjatrader.com/docs/desktop/chartanchor) representing the starting point of the drawing object |
| AreaOpacity | An int value representing the opacity of the area color |
| AreaBrush | A [Brush](http://msdn.microsoft.com/en-us/library/system.windows.media.brush(v=vs.110).aspx) object representing the fill color of the draw object |
| OutlineStroke | A Stroke used for the outline of the region |


## [Examples](https://developer.ninjatrader.com/docs/desktop/region#examples)


```csharp
// Instantiate a Region object
Region myRegion = Draw.Region(this, "tag1", CurrentBar, 0, Bollinger(2, 14).Upper, Bollinger(2, 14).Lower, null, Brushes.Blue, 50);

// Set the object's OutlineStroke to a new Stroke
myRegion.OutlineStroke = new Stroke(Brushes.Red, DashStyleHelper.Solid, 3);
```
