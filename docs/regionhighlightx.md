# RegionHighlightX

Source: https://developer.ninjatrader.com/docs/desktop/regionhighlightx

---

# RegionHighlightX


## [Definition](https://developer.ninjatrader.com/docs/desktop/regionhighlightx#definition)


Represents an interface that exposes information regarding a Region Highlight X **IDrawingTool**.


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/regionhighlightx#methods-and-properties)


| Parameter | Description |
| --- | --- |
| StartAnchor | An **IDrawingTool's ChartAnchor** representing the starting point of the drawing object |
| EndAnchor | An **IDrawingTool's ChartAnchor** representing the end point of the drawing object |
| AreaBrush | A **Brush** class representing the fill color of the draw object |
| AreaOpacity | An **int** value representing the opacity of the area color |
| OutlineStroke | The **Stroke** object used to draw the object's outline |


## [Examples](https://developer.ninjatrader.com/docs/desktop/regionhighlightx#examples)


```csharp
// Instantiate a RegionHighlightX object
RegionHighlightX myReg = Draw.RegionHighlightX(this, "tag1", 10, 0, Brushes.Blue);

// Change the object's opacity
myReg.AreaOpacity = 25;
```
