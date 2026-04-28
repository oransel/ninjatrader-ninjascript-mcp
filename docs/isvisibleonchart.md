# IsVisibleOnChart()

Source: https://developer.ninjatrader.com/docs/desktop/isvisibleonchart

---

# IsVisibleOnChart()


## [Definition](https://developer.ninjatrader.com/docs/desktop/isvisibleonchart#definition)


Indicates a chart object is visible on the chart. When the **IsVisibleOnChart()** method determines a chart object is not visible and returns false, the object will not be used in a render pass, will not be considered in a hit test, and will not be used for alerting. The base implementation is to always return true on all chart objects, however this behavior can be overridden for your custom object if desired.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/isvisibleonchart#method-return-value)


A virtual bool value which when true, the object will be rendered and can be interacted with by a user; otherwise false. Default value is true.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/isvisibleonchart#syntax)


You must override this method using the following syntax:


`public override bool IsVisibleOnChart(ChartControl chartControl, ChartScale chartScale, DateTime firstTimeOnChart, DateTime lastTimeOnChart)`


## [Method Parameters](https://developer.ninjatrader.com/docs/desktop/isvisibleonchart#method-parameters)


| --- |
| **chartControl** | A [ChartControl](https://developer.ninjatrader.com/docs/desktop/chartcontrol) representing the x-axis |
| **chartScale** | A [ChartScale](https://developer.ninjatrader.com/docs/desktop/chartscale) representing the y-axis |
| **firstTimeOnChart** | A DateTime representing the first painted bar displayed on the chart |
| **lastTimeOnChart** | A DateTime representing the last painted bar displayed on the chart |


## [Examples](https://developer.ninjatrader.com/docs/desktop/isvisibleonchart#examples)


```csharp
public override bool IsVisibleOnChart(ChartControl chartControl, ChartScale chartScale, DateTime firstTimeOnChart, DateTime lastTimeOnChart)
{
    // check if any chart anchors are visible
    foreach (ChartAnchor anchor in Anchors)
    {
        if (anchor.Time >= firstTimeOnChart && anchor.Time <= lastTimeOnChart)
            return true;
    }
    return false; // otherwise the object should not be displayed
}
```
