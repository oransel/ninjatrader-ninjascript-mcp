# IsAutoScale

Source: https://developer.ninjatrader.com/docs/desktop/isautoscale

---

# IsAutoScale


## [Definition](https://developer.ninjatrader.com/docs/desktop/isautoscale#definition)


If true, the object will call **CalculateMinMax()** in order to determine the object's **MinValue** and **MaxValue** value used to scale the Y-axis of the chart.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/isautoscale#property-value)


This property returns true if the object's are included in the y-scale; otherwise, false. Default set to false for **DrawingTools**, but set to true for **Indicators**.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


This property should ONLY be set from the **OnStateChange()** method during State.SetDefaults or State.Configure.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/isautoscale#syntax)


`IsAutoScale`


## [Examples](https://developer.ninjatrader.com/docs/desktop/isautoscale#examples)


```csharp
protected override void OnStateChange()
{
   if (State == State.SetDefaults)
   {
     Name                 = "Example Indicator";
     // set this to true to call CalculateMinMix() to ensure drawing tool is fully rendered in chart scale
     IsAutoScale = true;
   }
   else if (State == State.Configure)
   {
   }
}
```
