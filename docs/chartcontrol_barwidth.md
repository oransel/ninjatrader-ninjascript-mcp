# BarWidth

Source: https://developer.ninjatrader.com/docs/desktop/chartcontrol_barwidth

---

# BarWidth


## [Definition](https://developer.ninjatrader.com/docs/desktop/chartcontrol_barwidth#definition)


Measures the value of the **bar width** set for the primary Bars object on the chart.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This property value is not stated in pixels. To obtain the pixel-width of bars on the chart, use **GetBarPaintWidth()** instead.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/chartcontrol_barwidth#property-value)


A **double** representing the value of the bar width.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/chartcontrol_barwidth#syntax)


`<chartcontrol>.BarWidth`


## [Examples](https://developer.ninjatrader.com/docs/desktop/chartcontrol_barwidth#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
    double barWidth = chartControl.BarWidth;

    // Prints the width of bars on the chart
    Print(barWidth);
}
```


Based on the image below, BarWidth reveals that the bars on the chart are 4.02 pixels wide.


![ChartControl_BarWidth](https://cdn.sanity.io/images/1hlwceal/production/17998ce21ef3c4c2ec151b9e6d700c2023bfd841-534x429.png)
