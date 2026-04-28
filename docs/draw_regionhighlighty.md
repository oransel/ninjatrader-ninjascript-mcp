# Draw.RegionHighlightY()

Source: https://developer.ninjatrader.com/docs/desktop/draw_regionhighlighty

---

# Draw.RegionHighlightY()


## [Definition](https://developer.ninjatrader.com/docs/desktop/draw_regionhighlighty#definition)


Draws a region highlight y on a chart.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/draw_regionhighlighty#method-return-value)


A **[RegionHighlightY](https://developer.ninjatrader.com/docs/desktop/regionhighlighty)** object that represents the draw object.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/draw_regionhighlighty#syntax)


`Draw.RegionHighlightY(NinjaScriptBase owner, string tag, double startY, double endY, Brush brush)`


`Draw.RegionHighlightY(NinjaScriptBase owner, string tag, bool isAutoScale, double startY, double endY, Brush brush, Brush areaBrush, int areaOpacity)`


`Draw.RegionHighlightY(NinjaScriptBase owner, string tag, double startY, double endY, bool isGlobal, string templateName)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/draw_regionhighlighty#parameters)


| --- |
| owner | The hosting **NinjaScript** object which is calling the draw method. Typically will be the object which is calling the draw method (e.g., "this"). |
| tag | A user defined unique id used to reference the draw object. For example, if you pass in a value of "myTag", each time this tag is used, the same draw object is modified. If unique tags are used each time, a new draw object will be created each time. |
| isAutoScale | Determines if the draw object will be included in the y-axis scale. Default value is false. |
| startY | The starting y value co-ordinate where the draw object will be drawn. |
| endY | The ending y value co-ordinate where the draw object will be drawn. |
| brush | The brush used to color the outline of draw object ([reference](https://developer.ninjatrader.com/docs/desktop/brushes)). |
| areaBrush | The brush used to color the fill area of the draw object ([reference](https://developer.ninjatrader.com/docs/desktop/brushes)). |
| areaOpacity | Sets the level of transparency for the fill color. Valid values between 0 - 100. (0 = completely transparent, 100 = no opacity). |
| isGlobal | Determines if the draw object will be global across all charts which match the instrument. |
| templateName | The name of the drawing tool template the object will use to determine various visual properties (empty string could be used to just use the UI default visuals instead). |


## [Examples](https://developer.ninjatrader.com/docs/desktop/draw_regionhighlighty#examples)


```csharp
// Fills in the region between the startY and endY
Draw.RegionHighlightY(this, "tag1", true, High[0], Low[0], Brushes.Blue, Brushes.Green, 20);
```
