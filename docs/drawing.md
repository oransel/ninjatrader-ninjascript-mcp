# Drawing

Source: https://developer.ninjatrader.com/docs/desktop/drawing

---

# Drawing


You can use **NinjaScript** to draw custom shapes, lines, text and colors on price and indicator panels from both [Indicators](https://developer.ninjatrader.com/docs/desktop/indicators) and [Strategies](https://developer.ninjatrader.com/docs/desktop/strategies).


## [Draw Methods and Associated Return Types](https://developer.ninjatrader.com/docs/desktop/drawing#draw-methods-and-associated-return-types)


| Draw Method | Return Type |
| --- | --- |
| [Draw.AndrewsPitchfork()](https://developer.ninjatrader.com/docs/desktop/draw_andrewspitchfork) | [AndrewsPitchfork](https://developer.ninjatrader.com/docs/desktop/andrewspitchfork) |
| [Draw.Arc()](https://developer.ninjatrader.com/docs/desktop/draw_arc) | [Arc](https://developer.ninjatrader.com/docs/desktop/arc) |
| [Draw.ArrowDown()](https://developer.ninjatrader.com/docs/desktop/draw_arrowdown) | [ArrowDown](https://developer.ninjatrader.com/docs/desktop/arrowdown) |
| [Draw.ArrowLine()](https://developer.ninjatrader.com/docs/desktop/draw_arrowline) | [ArrowLine](https://developer.ninjatrader.com/docs/desktop/arrowline) |
| [Draw.ArrowUp()](https://developer.ninjatrader.com/docs/desktop/draw_arrowup) | [ArrowUp](https://developer.ninjatrader.com/docs/desktop/arrowup) |
| [Draw.Diamond()](https://developer.ninjatrader.com/docs/desktop/draw_diamond) | [Diamond](https://developer.ninjatrader.com/docs/desktop/diamond) |
| [Draw.Dot()](https://developer.ninjatrader.com/docs/desktop/draw_dot) | [Dot](https://developer.ninjatrader.com/docs/desktop/dot) |
| [Draw.Ellipse()](https://developer.ninjatrader.com/docs/desktop/draw_ellipse) | [Ellipse](https://developer.ninjatrader.com/docs/desktop/ellipse) |
| [Draw.ExtendedLine()](https://developer.ninjatrader.com/docs/desktop/draw_extendedline) | [ExtendedLine](https://developer.ninjatrader.com/docs/desktop/extendedline) |
| [Draw.FibonacciCircle()](https://developer.ninjatrader.com/docs/desktop/draw_fibonaccicircle) | [FibonacciCircle](https://developer.ninjatrader.com/docs/desktop/fibonaccicircle) |
| [Draw.FibonacciExtensions()](https://developer.ninjatrader.com/docs/desktop/draw_fibonacciextensions) | [FibonacciExtensions](https://developer.ninjatrader.com/docs/desktop/fibonacciextensions) |
| [Draw.FibonacciRetracements()](https://developer.ninjatrader.com/docs/desktop/draw_fibonacciretracements) | [FibonacciRetracements](https://developer.ninjatrader.com/docs/desktop/fibonacciretracements) |
| [Draw.FibonacciTimeExtensions()](https://developer.ninjatrader.com/docs/desktop/draw_fibonaccitimeextensions) | [FibonacciTimeExtensions](https://developer.ninjatrader.com/docs/desktop/fibonaccitimeextensions) |
| [Draw.GannFan()](https://developer.ninjatrader.com/docs/desktop/draw_gannfan) | [GannFan](https://developer.ninjatrader.com/docs/desktop/gannfan) |
| [Draw.HorizontalLine()](https://developer.ninjatrader.com/docs/desktop/draw_horizontal_line) | [HorizontalLine](https://developer.ninjatrader.com/docs/desktop/horizontalline) |
| [Draw.Line()](https://developer.ninjatrader.com/docs/desktop/draw_line) | [Line](https://developer.ninjatrader.com/docs/desktop/line) |
| [Draw.Pathtool()](https://developer.ninjatrader.com/docs/desktop/draw_pathtool) | [Pathtool](https://developer.ninjatrader.com/docs/desktop/pathtool) |
| [Draw.Polygon()](https://developer.ninjatrader.com/docs/desktop/draw_polygon) | [Polygon](https://developer.ninjatrader.com/docs/desktop/polygon) |
| [Draw.Ray()](https://developer.ninjatrader.com/docs/desktop/draw_ray) | [Ray](https://developer.ninjatrader.com/docs/desktop/ray) |
| [Draw.Rectangle()](https://developer.ninjatrader.com/docs/desktop/draw_rectangle) | [Rectangle](https://developer.ninjatrader.com/docs/desktop/rectangle) |
| [Draw.Region()](https://developer.ninjatrader.com/docs/desktop/draw_region) | [Region](https://developer.ninjatrader.com/docs/desktop/region) |
| [Draw.RegionHighlightX()](https://developer.ninjatrader.com/docs/desktop/draw_regionhighlightx) | [RegionHighlightX](https://developer.ninjatrader.com/docs/desktop/regionhighlightx) |
| [Draw.RegionHighlightY()](https://developer.ninjatrader.com/docs/desktop/draw_regionhighlighty) | [RegionHighlightY](https://developer.ninjatrader.com/docs/desktop/regionhighlighty) |
| [Draw.RegressionChannel()](https://developer.ninjatrader.com/docs/desktop/draw_regressionchannel) | [RegressionChannel](https://developer.ninjatrader.com/docs/desktop/regressionchannel) |
| [Draw.RiskReward()](https://developer.ninjatrader.com/docs/desktop/draw_riskreward) | [RiskReward](https://developer.ninjatrader.com/docs/desktop/riskreward) |
| [Draw.Ruler()](https://developer.ninjatrader.com/docs/desktop/draw_ruler) | [Ruler](https://developer.ninjatrader.com/docs/desktop/ruler) |
| [Draw.Square()](https://developer.ninjatrader.com/docs/desktop/draw_square) | [Square](https://developer.ninjatrader.com/docs/desktop/square) |
| [Draw.Text()](https://developer.ninjatrader.com/docs/desktop/draw_text) | [Text](https://developer.ninjatrader.com/docs/desktop/text) |
| [Draw.TextFixed()](https://developer.ninjatrader.com/docs/desktop/draw_textfixed) | [TextFixed](https://developer.ninjatrader.com/docs/desktop/textfixed) |
| [Draw.TimeCycles()](https://developer.ninjatrader.com/docs/desktop/draw_timecycles) | [TimeCycles](https://developer.ninjatrader.com/docs/desktop/timecycles) |
| [Draw.TrendChannel()](https://developer.ninjatrader.com/docs/desktop/draw_trendchannel) | [TrendChannel](https://developer.ninjatrader.com/docs/desktop/trendchannel) |
| [Draw.Triangle()](https://developer.ninjatrader.com/docs/desktop/draw_triangle) | [Triangle](https://developer.ninjatrader.com/docs/desktop/triangle) |
| [Draw.TriangleDown()](https://developer.ninjatrader.com/docs/desktop/draw_triangledown) | [TriangleDown](https://developer.ninjatrader.com/docs/desktop/triangledown) |
| [Draw.TriangleUp()](https://developer.ninjatrader.com/docs/desktop/draw_triangleup) | [TriangleUp](https://developer.ninjatrader.com/docs/desktop/triangleup) |
| [Draw.VerticalLine()](https://developer.ninjatrader.com/docs/desktop/draw_verticalline) | [VerticalLine](https://developer.ninjatrader.com/docs/desktop/verticalline) |


## [Drawing Methods and Properties](https://developer.ninjatrader.com/docs/desktop/drawing#drawing-methods-and-properties)


| Property | Description |
| --- | --- |
| [AllowRemovalOfDrawObjects](https://developer.ninjatrader.com/docs/desktop/allowremovalofdrawobjects) | Determines if programmatically drawn DrawObjects can be manually removed from the chart |
| [BackBrush](https://developer.ninjatrader.com/docs/desktop/backbrush) | Sets the brush used for painting the chart panel's background color for the current bar |
| [BackBrushAll](https://developer.ninjatrader.com/docs/desktop/backbrushall) | Sets the brush used for painting the chart's background color for the current bar |
| [BackBrushes](https://developer.ninjatrader.com/docs/desktop/backbrushes) | A collection of historical brushes used for the background colors for the chart panel |
| [BackBrushesAll](https://developer.ninjatrader.com/docs/desktop/backbrushesall) | A collection of historical brushes used for the background colors for all chart panels |
| [BarBrush](https://developer.ninjatrader.com/docs/desktop/barbrush) | Sets the brush used for painting the color of a price bar's body |
| [BarBrushes](https://developer.ninjatrader.com/docs/desktop/barbrushes) | A collection of historical brushes used for painting the color of a price bar's body |
| [Brushes](https://developer.ninjatrader.com/docs/desktop/brushes) | A collection of static, predefined Brushes supplied by the .NET Framework |
| [CandleOutlineBrush](https://developer.ninjatrader.com/docs/desktop/candleoutlinebrush) | Sets the outline Brush of a candlestick |
| [CandleOutlineBrushes](https://developer.ninjatrader.com/docs/desktop/candleoutlinebrushes) | A collection of historical outline brushes for candlesticks |
| [DrawObjects](https://developer.ninjatrader.com/docs/desktop/drawobjects) | A collection holding all of the drawn chart objects for the primary bar series |
| [IDrawingTool](https://developer.ninjatrader.com/docs/desktop/idrawingtool) | Represents an interface that exposes information regarding a drawn chart object |
| [RemoveDrawObject()](https://developer.ninjatrader.com/docs/desktop/removedrawobject) | Removes a draw object from the chart based on its tag value |
| [RemoveDrawObjects()](https://developer.ninjatrader.com/docs/desktop/removedrawobjects) | Removes all draw objects originating from the indicator or strategy from the chart |
| [SimpleFont Class](https://developer.ninjatrader.com/docs/desktop/simplefont) | Defines a particular font configuration |


- Custom graphics for custom indicators can be painted on either the price panel or indicator panel. You could for example have a custom indicator displayed in an indicator panel yet have associated custom graphics painted on the price panel. The "**DrawOnPricePanel**" property is set to true by default, which means that custom graphics will always be painted on the price panel, even if the indicator is plotted in a separate panel. If you want your custom graphics to be plotted on the indicator panel, set this property to false in the **OnStateChange()** method of your custom indicator.
- Set unique tag values for each draw object, unless you intend for new draw objects to replace existing objects with the same tag. A common trick is to incorporate the bar number as part of the unique tag identifier. For example, if you wanted to draw a dot that indicated a buying condition above a bar, you could express it: **Draw.Dot(this, CurrentBar.ToString() + "Buy", false, 0, High[0] + TickSize, Brushes.ForestGreen);**
- Draw methods will not work if they are called from the **OnStateChange()** method.
