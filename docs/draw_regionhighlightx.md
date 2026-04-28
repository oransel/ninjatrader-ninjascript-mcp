# Draw.RegionHighlightX()

Source: https://developer.ninjatrader.com/docs/desktop/draw_regionhighlightx

---

# Draw.RegionHighlightX()


## [Definition](https://developer.ninjatrader.com/docs/desktop/draw_regionhighlightx#definition)


Draws a region highlight x on a chart.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/draw_regionhighlightx#method-return-value)


A **[RegionHighlightX](https://developer.ninjatrader.com/docs/desktop/regionhighlightx)** object that represents the draw object.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/draw_regionhighlightx#syntax)


`Draw.RegionHighlightX(NinjaScriptBase owner, string tag, DateTime startTime, DateTime endTime, Brush brush)`


`Draw.RegionHighlightX(NinjaScriptBase owner, string tag, int startBarsAgo, int endBarsAgo, Brush brush)`


`Draw.RegionHighlightX(NinjaScriptBase owner, string tag, DateTime startTime, DateTime endTime, Brush brush, Brush areaBrush, int areaOpacity)`


`Draw.RegionHighlightX(NinjaScriptBase owner, string tag, int startBarsAgo, int endBarsAgo, Brush brush, Brush areaBrush, int areaOpacity)`


`Draw.RegionHighlightX(NinjaScriptBase owner, string tag, DateTime startTime, DateTime endTime, bool isGlobal, string templateName)`


`Draw.RegionHighlightX(NinjaScriptBase owner, string tag, int startBarsAgo, int endBarsAgo, bool isGlobal, string templateName)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/draw_regionhighlightx#parameters)


| --- |
| owner | The hosting **NinjaScript** object which is calling the draw method. Typically will be the object which is calling the draw method (e.g., "this"). |
| tag | A user defined unique id used to reference the draw object. For example, if you pass in a value of "myTag", each time this tag is used, the same draw object is modified. If unique tags are used each time, a new draw object will be created each time. |
| startBarsAgo | The starting bar (x axis co-ordinate) where the draw object will be drawn. For example, a value of 10 would paint the draw object 10 bars back. |
| startTime | The starting time where the draw object will be drawn. |
| endBarsAgo | The end bar (x axis co-ordinate) where the draw object will terminate. |
| endTime | The end time where the draw object will terminate. |
| brush | The brush used to color the outline of draw object ([reference](https://developer.ninjatrader.com/docs/desktop/brushes)). |
| areaBrush | The brush used to color the fill area of the draw object ([reference](https://developer.ninjatrader.com/docs/desktop/brushes)). |
| areaOpacity | Sets the level of transparency for the fill color. Valid values between 0 - 100. (0 = completely transparent, 100 = no opacity). |
| isGlobal | Determines if the draw object will be global across all charts which match the instrument. |
| templateName | The name of the drawing tool template the object will use to determine various visual properties (empty string could be used to just use the UI default visuals instead). |


## [Examples](https://developer.ninjatrader.com/docs/desktop/draw_regionhighlightx#examples)


```csharp
// Fills in the region between the startBar and endBar
Draw.RegionHighlightX(this, "tag1", 10, 0, rushes.Blue);
```
