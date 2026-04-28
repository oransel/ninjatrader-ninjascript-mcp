# Draw.VerticalLine()

Source: https://developer.ninjatrader.com/docs/desktop/draw_verticalline

---

# Draw.VerticalLine()


## [Definition](https://developer.ninjatrader.com/docs/desktop/draw_verticalline#definition)


Draws a vertical line.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/draw_verticalline#method-return-value)


A **[VerticalLine](https://developer.ninjatrader.com/docs/desktop/verticalline)** object that represents the draw object.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/draw_verticalline#syntax)


`Draw.VerticalLine(NinjaScriptBase owner, string tag, DateTime time, Brush brush)`


`Draw.VerticalLine(NinjaScriptBase owner, string tag, DateTime time, Brush brush, DashStyleHelper dashStyle, int width, bool drawOnPricePanel)`


`Draw.VerticalLine(NinjaScriptBase owner, string tag, int barsAgo, Brush brush)`


`Draw.VerticalLine(NinjaScriptBase owner, string tag, int barsAgo, Brush brush, DashStyleHelper dashStyle, int width, bool drawOnPricePanel)`


`Draw.VerticalLine(NinjaScriptBase owner, string tag, int barsAgo, bool isGlobal, string templateName)`


`Draw.VerticalLine(NinjaScriptBase owner, string tag, DateTime time, bool isGlobal, string templateName)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/draw_verticalline#parameters)


| --- |
| owner | The hosting **NinjaScript** object which is calling the draw method. Typically will be the object which is calling the draw method (e.g., "this"). |
| tag | A user defined unique id used to reference the draw object. For example, if you pass in a value of "myTag", each time this tag is used, the same draw object is modified. If unique tags are used each time, a new draw object will be created each time. |
| barsAgo | The bar the object will be drawn at. A value of 10 would be 10 bars ago. |
| time | The time the object will be drawn at. |
| brush | The brush used to color draw object ([reference](https://msdn.microsoft.com/en-us/library/system.windows.media.brushes%28v=vs.110%29.aspx)). |
| dashStyle | Possible values include:

- **DashStyleHelper.Dash**,
- **DashStyleHelper.DashDot**,
- **DashStyleHelper.DashDotDot**,
- **DashStyleHelper.Dot**,
- **DashStyleHelper.Solid**. |
| width | The width of the draw object. |
| drawOnPricePanel | Determines if the draw-object should be on the price panel or a separate panel. |
| isGlobal | Determines if the draw object will be global across all charts which match the instrument. |
| templateName | The name of the drawing tool template the object will use to determine various visual properties (empty string could be used to just use the UI default visuals instead). |

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Drawing objects with y values very far off the visible canvas can lead to performance hits. Fancier DashStyles like **DashDotDot** will also require more resources than simple DashStyles like **Solid**.


## [Examples](https://developer.ninjatrader.com/docs/desktop/draw_verticalline#examples)


```csharp
// Draws a vertical line
Draw.VerticalLine(this, "tag1", 10, Brushes.Black);
```
