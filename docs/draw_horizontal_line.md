# Draw.HorizontalLine()

Source: https://developer.ninjatrader.com/docs/desktop/draw_horizontal_line

---

# Draw.HorizontalLine()


## [Definition](https://developer.ninjatrader.com/docs/desktop/draw_horizontal_line#definition)


Draws a horizontal line.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/draw_horizontal_line#method-return-value)


A **[HorizontalLine](https://developer.ninjatrader.com/docs/desktop/horizontalline)** object that represents the draw object.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/draw_horizontal_line#syntax)


`Draw.HorizontalLine(NinjaScriptBase owner, string tag, double y, Brush brush)`


`Draw.HorizontalLine(NinjaScriptBase owner, string tag, bool isAutoScale, double y, Brush brush, DashStyleHelper dashStyle, int width)`


`Draw.HorizontalLine(NinjaScriptBase owner, string tag, bool isAutoscale, double y, Brush brush, bool drawOnPricePanel)`


`Draw.HorizontalLine(NinjaScriptBase owner, string tag, double y, Brush brush, DashStyleHelper dashStyle, int width, bool drawOnPricePanel)`


`Draw.HorizontalLine(NinjaScriptBase owner, string tag, double y, bool isGlobal, string templateName)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/draw_horizontal_line#parameters)


| --- |
| owner | The hosting **NinjaScript** object which is calling the draw method. Typically will be the object which is calling the draw method (e.g., "this"). |
| tag | A user defined unique id used to reference the draw object. For example, if you pass in a value of "myTag", each time this tag is used, the same draw object is modified. If unique tags are used each time, a new draw object will be created each time. |
| isAutoScale | Determines if the draw object will be included in the y-axis scale. Default value is false. |
| y | The y value. |
| brush | The brush used to color draw object ([reference](https://developer.ninjatrader.com/docs/desktop/brushes)). |
| dashStyle | Possible values include:

- **DashStyleHelper.Dash**,
- **DashStyleHelper.DashDot**,
- **DashStyleHelper.DashDotDot**,
- **DashStyleHelper.Dot**,
- **DashStyleHelper.Solid**. |
| width | The width of the draw object. |
| isDrawOnPricePanel | Determines if the draw-object should be on the price panel or a separate panel. |
| isGlobal | Determines if the draw object will be global across all charts which match the instrument. |
| templateName | The name of the drawing tool template the object will use to determine various visual properties (empty string could be used to just use the UI default visuals instead). |

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Drawing objects with y values very far off the visible canvas can lead to performance hits. Fancier DashStyles like **DashDotDot** will also require more resources than simple DashStyles like **Solid**.


## [Examples](https://developer.ninjatrader.com/docs/desktop/draw_horizontal_line#examples)


```csharp
// Draws a horizontal line
Draw.HorizontalLine(this, "tag1", 1000, Brushes.Black);
```
