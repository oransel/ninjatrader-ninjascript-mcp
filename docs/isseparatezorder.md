# IsSeparateZOrder

Source: https://developer.ninjatrader.com/docs/desktop/isseparatezorder

---

# IsSeparateZOrder


## [Definition](https://developer.ninjatrader.com/docs/desktop/isseparatezorder#definition)


Determines the [ZOrder](https://developer.ninjatrader.com/docs/desktop/chart_zorder) of the drawing object will be different than the NinjaScript object that drew it.  When false the drawing object will share the same ZOrder.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/isseparatezorder#property-value)


This property returns true if the object is drawn on a separate ZOrder; otherwise, false. Default set to false.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/isseparatezorder#syntax)


`IsSeparateZOrder`


## [Example](https://developer.ninjatrader.com/docs/desktop/isseparatezorder#example)


```csharp
protected override void OnBarUpdate()
{
  // Instantiate a Dot object
  Dot myDot = Draw.Dot(this, "NewDot", true, 5, High[5], Brushes.Black);
 
  // Set the Dot object to use a separate Z-Order than the indicator that created it
  myDot.IsSeparateZOrder = true;
}
```
