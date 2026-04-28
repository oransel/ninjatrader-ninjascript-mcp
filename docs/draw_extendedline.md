# Draw.ExtendedLine()

Source: https://developer.ninjatrader.com/docs/desktop/draw_extendedline

---

# Draw.ExtendedLine()


## [Definition](https://developer.ninjatrader.com/docs/desktop/draw_extendedline#definition)


Draws a line with infinite end points.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/draw_extendedline#method-return-value)


An **[ExtendedLine](https://developer.ninjatrader.com/docs/desktop/extendedline)** object that represents the draw object.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/draw_extendedline#syntax)


`Draw.ExtendedLine(NinjaScriptBase owner, string tag, int startBarsAgo, double startY, int endBarsAgo, double endY, Brush brush)`


`Draw.ExtendedLine(NinjaScriptBase owner, string tag, DateTime startTime, double startY, DateTime endTime, double endY, Brush brush)`


`Draw.ExtendedLine(NinjaScriptBase owner, string tag, bool isAutoScale, int startBarsAgo, double startY, int endBarsAgo, double endY, Brush brush, DashStyleHelper dashStyle, int width)`


`Draw.ExtendedLine(NinjaScriptBase owner, string tag, bool isAutoScale, DateTime startTime, double startY, DateTime endTime, double endY, Brush brush, DashStyleHelper dashStyle, int width)`


`Draw.ExtendedLine(NinjaScriptBase owner, string tag, bool isAutoScale, int startBarsAgo, double startY, int endBarsAgo, double endY, Brush brush, DashStyleHelper dashStyle, int width, bool drawOnPricePanel)`


`Draw.ExtendedLine(NinjaScriptBase owner, string tag, bool isAutoScale, DateTime startTime, double startY, DateTime endTime, double endY, Brush brush, DashStyleHelper dashStyle, int width, bool drawOnPricePanel)`


`Draw.ExtendedLine(NinjaScriptBase owner, string tag, int startBarsAgo, double startY, int endBarsAgo, double endY, bool isGlobal, string templateName)`


`Draw.ExtendedLine(NinjaScriptBase owner, string tag, DateTime startTime, double startY, DateTime endTime, double endY, bool isGlobal, string templateName)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/draw_extendedline#parameters)


| --- |
| owner | The hosting **NinjaScript** object which is calling the draw method. Typically will be the object which is calling the draw method (e.g., "this"). |
| tag | A user defined unique id used to reference the draw object. For example, if you pass in a value of "myTag", each time this tag is used, the same draw object is modified. If unique tags are used each time, a new draw object will be created each time. |
| isAutoScale | Determines if the draw object will be included in the y-axis scale. Default value is false. |
| startBarsAgo | The starting bar (x axis co-ordinate) where the draw object will be drawn. For example, a value of 10 would paint the draw object 10 bars back. |
| startTime | The starting time where the draw object will be drawn. |
| startY | The starting y value co-ordinate where the draw object will be drawn. |
| endBarsAgo | The end bar (x axis co-ordinate) where the draw object will terminate. |
| endTime | The end time where the draw object will terminate. |
| endY | The end y value co-ordinate where the draw object will terminate. |
| brush | The brush used to color draw object ([reference](https://developer.ninjatrader.com/docs/desktop/brushes)). |
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


## [Examples](https://developer.ninjatrader.com/docs/desktop/draw_extendedline#examples)


```csharp
// Draws a dotted lime green
Draw.ExtendedLine(this, "tag1", 10, Close[10], 0, Close[0], Brushes.LimeGreen, DashStyleHelper.Dot, 2);
```
