# IsXPropertiesVisible

Source: https://developer.ninjatrader.com/docs/desktop/isxpropertiesvisible

---

# IsXPropertiesVisible


## [Definition](https://developer.ninjatrader.com/docs/desktop/isxpropertiesvisible#definition)


Indicates the anchor's X properties are visible on the UI. When set to true, the X values can be viewed from the Drawing Objects properties.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/isxpropertiesvisible#property-value)


A bool value which when true will display the anchor's X (time) data values from the drawing object properties; otherwise false. Default value is true.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/isxpropertiesvisible#syntax)


`<chartanchor>.IsXPropertiesVisible`


## [Examples](https://developer.ninjatrader.com/docs/desktop/isxpropertiesvisible#examples)


```csharp
protected override void OnStateChange()
{
     if (State == State.SetDefaults)
     {
         MyAnchor = new ChartAnchor();
         MyAnchor.IsXPropertiesVisible = true;
     }
     else if (State == State.Configure)
     {

     }
}
```
