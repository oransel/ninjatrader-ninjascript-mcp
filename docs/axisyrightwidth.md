# AxisYRightWidth

Source: https://developer.ninjatrader.com/docs/desktop/axisyrightwidth

---

# AxisYRightWidth


## [Definition](https://developer.ninjatrader.com/docs/desktop/axisyrightwidth#definition)


Measures the distance (in pixels) between the y-axis and the right edge of a chart.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/axisyrightwidth#property-value)


A double representing the number of pixels separating the y-axis and the right edge of the chart.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/axisyrightwidth#syntax)


`<chartcontrol>.AxisYRightWidth`


## [Example](https://developer.ninjatrader.com/docs/desktop/axisyrightwidth#example)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
     // Print the number of pixels between the y-axis and the right edge of the chart
     double rightWidth = chartControl.AxisYRightWidth;
     Print(rightWidth);
}
```


Based on the image below, AxisYRightWidth reveals that the space between the y-axis and the right edge of the chart is 53 pixels on this chart.


![ChartControl_AxisYRightWidth](https://cdn.sanity.io/images/1hlwceal/production/0f4affdc130fe1543d4a04caf22fa818ece905a1-534x429.png)
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


When there are no right-justified data series on a chart, AxisYRightWidth will return 0, as there will be no space between the y-axis and the right edge.
