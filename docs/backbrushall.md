# BackBrushAll

Source: https://developer.ninjatrader.com/docs/desktop/backbrushall

---

# BackBrushAll


## [Definition](https://developer.ninjatrader.com/docs/desktop/backbrushall#definition)


A collection of prior back brushes used for the background colors for all chart panels.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/backbrushall#property-value)


A Brush object that represents the color of the current chart bar.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


To reset the Chart background color to the default background color property, set the BackBrushAll to null for that bar.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/backbrushall#syntax)


BackBrushAll
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


You may have up to 65,535 unique BackBrushAll instances, therefore, using static predefined brushes should be favored. Alternatively, in order to use fewer brushes, please try to cache your custom brushes until a new brush would actually need to be created.


## [Examples](https://developer.ninjatrader.com/docs/desktop/backbrushall#examples)


```csharp
protected override void OnBarUpdate()
{
     // Sets the back color to pale green
     BackBrushAll = Brushes.PaleGreen;

     // Sets the back color to null to use the default color set in the chart properties dialog window
     BackBrushAll = null;

     // Sets the back color to pink when the closing price is less than the 20 period SMA
     // and to lime green when above (see image below)
     BackBrushAll = SMA(20)[0] >= Close[0] ? Brushes.Pink : Brushes.PaleGreen;
}
```


![MAPriceBars2](https://cdn.sanity.io/images/1hlwceal/production/0b8055e8237bf5e30ddd6a5886c486f99f05e9f5-575x595.png)
