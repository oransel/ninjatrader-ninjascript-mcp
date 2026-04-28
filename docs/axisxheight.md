# AxisXHeight

Source: https://developer.ninjatrader.com/docs/desktop/axisxheight

---

# AxisXHeight


## [Definition](https://developer.ninjatrader.com/docs/desktop/axisxheight#definition)


Measures the distance (in pixels) between the x-axis and the top of the horizontal scroll bar near the bottom of the chart.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/axisxheight#property-value)


A double representing the number of pixels separating the x-axis and the top of the horizontal scroll bar on the chart.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/axisxheight#syntax)


`ChartControl.AxisXHeight`


## [Example](https://developer.ninjatrader.com/docs/desktop/axisxheight#example)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
     // Print the number of pixels between the x-axis and the top of the horizontal scrollbar
     double height = chartControl.AxisXHeight;
     Print(height);
}
```


Based on the image below, AxisXHeight reveals that the space between the x-axis and the top of the horizontal scrollbar is 31 pixels on this chart.


![ChartControl_AxisXHeight](https://cdn.sanity.io/images/1hlwceal/production/8be3b4d4a088a06870d4dfe1ae9ff2d8df7c7219-530x431.png)
