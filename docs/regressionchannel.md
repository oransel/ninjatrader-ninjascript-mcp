# RegressionChannel

Source: https://developer.ninjatrader.com/docs/desktop/regressionchannel

---

# RegressionChannel


## [Definition](https://developer.ninjatrader.com/docs/desktop/regressionchannel#definition)


Represents an interface that exposes information regarding a Regression Channel **IDrawingTool**.


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/regressionchannel#methods-and-properties)


| Parameter | Description |
| --- | --- |
| StartAnchor | An **IDrawingTool's ChartAnchor** representing the starting point of the drawing object |
| EndAnchor | An **IDrawingTool's ChartAnchor** representing the starting point of the drawing object |
| RegressionStroke | The **Stroke** object used to draw the middle line of the object |
| LowerChannelStroke | The **Stroke** object used to draw the lower line of the object |
| UpperChannelStroke | The **Stroke** object used to draw the upper line of the object |
| PriceType | Possible values are:


- **PriceType.Close**
- **PriceType.High**
- **PriceType.Low**
- **PriceType.Median**
- **PriceType.Open**
- **PriceType.Typical** |
| ChannelType | An enum value representing if the object will use standard deviations calculations for the upper/lower lines. Possible values are: | **RegressionChannelType.Segment** | **RegressionChannelType.StandardDeviation** |
| ExtendLeft | A bool value representing if the object will extend to the left |
| ExtendRight | A bool value representing if the object will extend to the right |
| StandardDeviationLowerDistance | A double value representing the standard deviation distance to the lower line |
| StandardDeviationUpperDistance | A double value representing the standard deviation distance to the upper line |


## [Examples](https://developer.ninjatrader.com/docs/desktop/regressionchannel#examples)


```csharp
// Instantiate a RegressionChannel object
NinjaTrader.NinjaScript.DrawingTools.RegressionChannel myRegChan = Draw.RegressionChannel(this, "tag1", 10, 0, Brushes.Blue);

// Change the object's PriceType
myRegChan.PriceType = PriceType.Median;
```

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


To differentiate between **DrawingTools.RegressionChannel** and **Indicators.RegressionChannel** when assigning a RegressionChannel object, you will need to invoke the former path explicitly, as seen in the example above.
