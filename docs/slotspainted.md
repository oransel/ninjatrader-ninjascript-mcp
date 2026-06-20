# SlotsPainted

Source: https://developer.ninjatrader.com/docs/desktop/slotspainted

---

# SlotsPainted


## [Definition](https://developer.ninjatrader.com/docs/desktop/slotspainted#definition)


Indicates the number of index slots in which bars are painted within the chart canvas area. This covers the visible portion of the chart only, and does not include historical painted bars outside of the visible area.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/slotspainted#property-value)


An int representing the number of index slots in which bars are painted.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/slotspainted#syntax)


`<chartcontrol>.SlotsPainted`


## [Examples](https://developer.ninjatrader.com/docs/desktop/slotspainted#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
   int painted = chartControl.SlotsPainted;
 
   // Print the number of bars painted on the visible chart canvas
   Print(painted);
}
```


In the image below, **SlotsPainted** reveals that there are 17 bars painted on the chart canvas.


![ChartControl_SlotsPainted](https://cdn.sanity.io/images/1hlwceal/production/a6e80e77cacce15553e0a1a5ee4abbeb9bd7f3f4-531x431.png)
