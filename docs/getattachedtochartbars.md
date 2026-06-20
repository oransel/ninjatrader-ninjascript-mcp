# GetAttachedToChartBars()

Source: https://developer.ninjatrader.com/docs/desktop/getattachedtochartbars

---

# GetAttachedToChartBars()


## [Definition](https://developer.ninjatrader.com/docs/desktop/getattachedtochartbars#definition)


Returns information which relate to the underlying bars series in which the drawing tool is attached. If the drawing tool is attached to an indicator rather than a bar series, the indicator's bars series used for input will be returned.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


For drawing tools made global, this method will not be returning meaningful values - since those are not attached to a specific bars series.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/getattachedtochartbars#method-return-value)


A **ChartBars** object


## [Syntax](https://developer.ninjatrader.com/docs/desktop/getattachedtochartbars#syntax)


`GetAttachedToChartBars()`


## [Method Parameters](https://developer.ninjatrader.com/docs/desktop/getattachedtochartbars#method-parameters)


This method does not accept any parameters.


## [Examples](https://developer.ninjatrader.com/docs/desktop/getattachedtochartbars#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{  
   // get the attached chart bars
   ChartBars myBars = GetAttachedToChartBars();
  
   Print(myBars.Bars.ToChartString()); // NQ 03-15 (1 Minute)
}
```
