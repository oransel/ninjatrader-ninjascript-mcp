# IsInHitTest

Source: https://developer.ninjatrader.com/docs/desktop/isinhittest

---

# IsInHitTest


## [Definition](https://developer.ninjatrader.com/docs/desktop/isinhittest#definition)


Indicates a user is currently clicking in the chart panel in which the calling script resides.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


In addition to the example below, **IsInHitTest** can also be tested directly on chart objects (for example, **myHorizontalLine.IsInHitTest**). In this case, the **IsInHitTest** property of a specific object will refer to the panel in which the calling script resides, even if the calling script resides in a different panel than the object itself.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/isinhittest#property-value)


This property returns true to indicate that the chart panel in which the script resides is being clicked on; otherwise, false. Default set to false.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/isinhittest#syntax)


`IsInHitTest`


## [Examples](https://developer.ninjatrader.com/docs/desktop/isinhittest#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
   if(IsInHitTest)
   {
       Print("user clicked on object");

       // do something
   }
}
```
