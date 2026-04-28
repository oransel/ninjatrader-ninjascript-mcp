# Draw.Dot()

Source: https://developer.ninjatrader.com/docs/desktop/draw_dot

---

# Draw.Dot()


## [Definition](https://developer.ninjatrader.com/docs/desktop/draw_dot#definition)


Draws a dot.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/draw_dot#method-return-value)


A **[Dot](https://developer.ninjatrader.com/docs/desktop/dot)** object that represents the draw object.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/draw_dot#syntax)


`Draw.Dot(NinjaScriptBase owner, string tag, bool isAutoScale, DateTime time, double y, Brush brush)`


`Draw.Dot(NinjaScriptBase owner, string tag, bool isAutoScale, int barsAgo, double y, Brush brush)`


`Draw.Dot(NinjaScriptBase owner, string tag, bool isAutoScale, DateTime time, double y, Brush brush, bool drawOnPricePanel)`


`Draw.Dot(NinjaScriptBase owner, string tag, bool isAutoScale, int barsAgo, double y, Brush brush, bool drawOnPricePanel)`


`Draw.Dot(NinjaScriptBase owner, string tag, bool isAutoScale, DateTime time, double y, bool isGlobal, string templateName)`


`Draw.Dot(NinjaScriptBase owner, string tag, bool isAutoScale, int barsAgo, double y, bool isGlobal, string templateName)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/draw_dot#parameters)


| --- |
| owner | The hosting **NinjaScript** object which is calling the draw method. Typically will be the object which is calling the draw method (e.g., "this"). |
| tag | A user defined unique id used to reference the draw object. For example, if you pass in a value of "myTag", each time this tag is used, the same draw object is modified. If unique tags are used each time, a new draw object will be created each time. |
| isAutoScale | Determines if the draw object will be included in the y-axis scale. |
| barsAgo | The bar the object will be drawn at. A value of 10 would be 10 bars ago. |
| time | The time the object will be drawn at. |
| y | The y value. |
| brush | The brush used to color draw object ([reference](https://developer.ninjatrader.com/docs/desktop/brushes)). |
| drawOnPricePanel | Determines if the draw-object should be on the price panel or a separate panel. |
| isGlobal | Determines if the draw object will be global across all charts which match the instrument. |
| templateName | The name of the drawing tool template the object will use to determine various visual properties (empty string could be used to just use the UI default visuals instead). |

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Tip: The size of the dot is tied to the chart's BarWidth and thus will scale automatically as the chart is resized.


## [Examples](https://developer.ninjatrader.com/docs/desktop/draw_dot#examples)


```csharp
// Paints a red dot on the current bar 1 tick below the low
Draw.Dot(this, "tag1", true, 0, Low[0] - TickSize, Brushes.Red);
```
