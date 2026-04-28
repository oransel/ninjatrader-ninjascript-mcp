# SlotIndex

Source: https://developer.ninjatrader.com/docs/desktop/barindex

---

# SlotIndex


## [Definition](https://developer.ninjatrader.com/docs/desktop/barindex#definition)


Indicates the nearest bar slot value where anchor is drawn on a chart. In a single series chart there will always be equal number of slots and bars, however for multi-series charts there may be additional slots compared to the bar series your drawing tool resides.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/barindex#property-value)


A **double** value representing the current bar.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


The bar index value is represented as a double as it is possible (and likely) that a given chart anchor is drawn between bars (i.e., if a user draws the tool with snap mode disabled)


## [Syntax](https://developer.ninjatrader.com/docs/desktop/barindex#syntax)


`ChartAnchor.SlotIndex`


## [Examples](https://developer.ninjatrader.com/docs/desktop/barindex#examples)


```csharp
public override void OnMouseDown(ChartControl chartControl, ChartPanel chartPanel, ChartScale chartScale, ChartAnchor dataPoint)
{
   Print(MyAnchor.SlotIndex); // prints the nearest current bar value
   //4502.02734375
}
```
