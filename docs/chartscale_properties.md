# Properties

Source: https://developer.ninjatrader.com/docs/desktop/chartscale_properties

---

# Properties


## [Definition](https://developer.ninjatrader.com/docs/desktop/chartscale_properties#definition)


Represents a number of properties available to the Chart Scale which can be configured to change the appearance of the scale.


![ChartPanel_Properites](https://cdn.sanity.io/images/1hlwceal/production/d54a7090533d4bbf1dccccf065ab3a3b503f0d83-450x425.png)
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


These are UI properties which are designed to be set by a user. Attempting to modify these values through a custom script is NOT guaranteed to take effect.


## [Property Values](https://developer.ninjatrader.com/docs/desktop/chartscale_properties#property-values)


| Property | Description |
| --- | --- |
| **YAxisRangeType** | An **YAxisRangeType** enum, possible values are:

- Automatic
- Fixed |
| **AutoScaleDateRangeType** | An **AutoScaleDateRangeType** enum, possible values are:

- ScreenDateRange
- EntireDateRangeSeriesOnly |
| **HorizontalGridlinesCalculation** | An **YAxisRangeType** enum, possible values are:

- Automatic
- Fixed |
| **HorizontalGridlinesIntervalType** | A **HorizontalGridlinesIntervalType** enum, possible values are:

- Ticks
- Points
- Pips |
| **HorizontalGridlinesInterval** | A **double** value representing the vertical interval of the horizontal axis |
| **AutoScaleMarginType** | An **AutoScaleMarginType** enum, possible values are:

- Percent
- Price |
| **AutoScaleMarginLower** | A **double** value representing the lowest margin used for the chart scale |
| **AutoScaleMarginUpper** | A **double** value representing the highest margin used for the chart scale |
| **YAxisScalingType** | An **YAxisScalingType** enum, possible values are:

- Linear
- Logarithmic |
| **FixedScaleMax** | A double representing the highest series value used for the chart scale when the scale is fixed |
| **FixedScaleMin** | A double representing the lowest series value used for the chart scale when the scale is fixed |


## [Syntax](https://developer.ninjatrader.com/docs/desktop/chartscale_properties#syntax)


`<chartscale>.Properties`


## [Examples](https://developer.ninjatrader.com/docs/desktop/chartscale_properties#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
    if (chartScale.Properties.YAxisScalingType == AxisScalingTypeLinear)
    {
        // do something
    }
}
```
