# IsScrollArrowVisible

Source: https://developer.ninjatrader.com/docs/desktop/isscrollarrowvisible

---

# IsScrollArrowVisible


## [Definition](https://developer.ninjatrader.com/docs/desktop/isscrollarrowvisible#definition)


Indicates the time-axis scroll arrow is visible in the top-right corner of the chart.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/isscrollarrowvisible#property-value)


A bool value. When **True**, indicates that the scroll arrow is visible on the chart; otherwise **False**.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/isscrollarrowvisible#syntax)


`<chartcontrol>.IsScrollArrowVisible`


## [Examples](https://developer.ninjatrader.com/docs/desktop/isscrollarrowvisible#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
   // Print a message if the scroll arrow is visible on the chart
   if(chartControl.IsScrollArrowVisible);
       Print("The chart is currently not set to auto-scroll. Click the scroll arrow to return to auto-scrolling");
}
```


Based on the image below, **IsScrollArrowVisible** confirms that the scroll arrow is currently visible on the chart.


![ChartControl_IsScrollArrowVisible](https://cdn.sanity.io/images/1hlwceal/production/0bb6ecfae5d7d73ec5d529ebd0c44f4c454d7c25-569x423.png)
