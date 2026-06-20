# IsVisible

Source: https://developer.ninjatrader.com/docs/desktop/isvisible

---

# IsVisible


## [Definition](https://developer.ninjatrader.com/docs/desktop/isvisible#definition)


Determines if the current **NinjaScript** object should be visible on the chart. When an object's **IsVisible** property is set to false, the object will NOT be displayed on the chart and will not be calculated to save resources.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Strategies intentionally contain no **IsVisible** property.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


This property should NOT be set on indicators which add a panel or own their own panel. Panel addition/removal is determined when an indicator is added/removed to a chart and is not modified through the **IsVisible** property.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/isvisible#property-value)


A bool value when true will be displayed on the chart; otherwise false; default value is true.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/isvisible#syntax)


`IsVisible`


## [Examples](https://developer.ninjatrader.com/docs/desktop/isvisible#examples)


```csharp
protected override void OnBarUpdate()
{
   // Loops through the DrawObjects collection via a threadsafe list copy
   foreach (DrawingTool draw in DrawObjects.ToList())
   {
     // Detect all manual drawn line objects and change their visibility
     if (draw is DrawingTools.Line && draw.IsUserDrawn)
     {
         draw.IsVisible = false;
     }
   }            
}
```
