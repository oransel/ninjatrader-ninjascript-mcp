# BackBrush

Source: https://developer.ninjatrader.com/docs/desktop/backbrush

---

# BackBrush


## [Definition](https://developer.ninjatrader.com/docs/desktop/backbrush#definition)


Sets the brush used for painting the chart panel's background color for the current bar.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This property will only set the back color for the panel the indicator is running. To set background color for all panels, please see the [BackBrushAll](https://developer.ninjatrader.com/docs/desktop/backbrushall) property.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/backbrush#property-value)


A [Brush](http://msdn.microsoft.com/en-us/library/system.windows.media.brush(v=vs.110).aspx) object that represents the color of the current chart bar.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/backbrush#syntax)


`BackBrush`
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


You may have up to 65,535 unique `BackBrush` instances, therefore, using [static predefined brushes](https://developer.ninjatrader.com/docs/desktop/working_with_brushes) should be favored. Alternatively, in order to use fewer brushes, please try to cache your custom brushes until a new brush would actually need to be created.


## [Examples](https://developer.ninjatrader.com/docs/desktop/backbrush#examples)


```csharp
protected override void OnBarUpdate()
{
     // Sets the chart panel back color to pale green
     BackBrush = Brushes.PaleGreen;

     // Sets the back color to to null which will use the default color set in the chart properties dialog window
     BackBrush = null;

     // Sets the back color to maroon when the closing price is less than the 20 period SMA // and to lime green when above (see image below)
     BackBrush = SMA(20)[0] >= Close[0] ? Brushes.Maroon : Brushes.LimeGreen;
}
```


![MAPriceBars](https://cdn.sanity.io/images/1hlwceal/production/81fc3cbedc3e8a75a3fd3a50fae1225d03f73e5c-575x518.png)
