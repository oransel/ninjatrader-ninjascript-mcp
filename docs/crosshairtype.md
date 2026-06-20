# CrosshairType

Source: https://developer.ninjatrader.com/docs/desktop/crosshairtype

---

# CrosshairType


## [Definition](https://developer.ninjatrader.com/docs/desktop/crosshairtype#definition)


Indicates the **Cross Hair** type currently enabled on the chart.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/crosshairtype#property-value)


An enum specifying the type of Cross Hair currently enabled on the chart. Possible values are listed below:


| --- |
| Local | The local (single-chart) Cross Hair is enabled |
| Global | Global Cross Hair |
| GlobalNoTimeScroll | Global Cross Hair (No Time Scroll) is enabled |


## [Syntax](https://developer.ninjatrader.com/docs/desktop/crosshairtype#syntax)


`<chartcontrol>.CrosshairType`


## [Examples](https://developer.ninjatrader.com/docs/desktop/crosshairtype#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
   // Print a message if the user enables the Global Cross Hair without time scrolling
   if (chartControl.CrosshairType == CrosshairType.GlobalNoTimeScroll)
       Print("It is recommended to enable Global Cross Hair time scrolling with this indicator");
}
```


In the image below, **CrosshairType** reveals that Global Cross Hair (No Time Scroll) is enabled on the chart.


![ChartControl_CrosshairType](https://cdn.sanity.io/images/1hlwceal/production/35287e4a3b87e5ac94a38146f3b7ac8689ce2c98-866x529.png)
