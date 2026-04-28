# Slope()

Source: https://developer.ninjatrader.com/docs/desktop/slope

---

# Slope()


## [Definition](https://developer.ninjatrader.com/docs/desktop/slope#definition)


Returns a measurement of the steepness of a price series (y value) measured by the change over time (x value). The return value can also be thought of as the ratio between the **startBarsAgo** and `endBarsAgo` parameters passed to the method.


The formula which is returned from the parameters passed is:


(series[`endBarsAgo`] - series[**startBarsAgo**]) / (**startBarsAgo** - **endBarsAgo**)
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


The return value should NOT be confused with the angle (or radians) of a line that displays on the chart.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/slope#method-return-value)


This method returns A **double** value indicating the slope of a line; A value of 0 returns if either the **startBars** or **endBars** parameters are less than 0 or both parameters are of equal value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/slope#syntax)


`Slope(ISeries<double> series, int startBarsAgo, int endBarsAgo)`
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


The "**startBarsAgo**" parameter MUST be greater than the "**endBarsAgo**" parameter.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/slope#parameters)


| Parameter | Description |
| --- | --- |
| **series** | Any **Series<`double`>** type object such as an indicator, Close, High, Low, etc... |
| **startBarsAgo** | The starting point of a series to be evaluated |
| **endBarsAgo** | The ending point of a series to be evaluated |

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Thinking in degrees, for example a 1 to -1 return range would translate to 45 to -45. To convert you could look into working with this formula - **Math.Atan(Slope)** * 180 / **Math.PI**.


## [Examples](https://developer.ninjatrader.com/docs/desktop/slope#examples)


```csharp
protected override void OnBarUpdate()
{
    // Prints the slope of the 20 period simple moving average of the last 10 bars
    Print(Slope(SMA(20), 10, 0));
}
```
