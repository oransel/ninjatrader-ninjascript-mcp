# ChartPanels

Source: https://developer.ninjatrader.com/docs/desktop/chartpanels

---

# ChartPanels


## [Definition](https://developer.ninjatrader.com/docs/desktop/chartpanels#definition)


Holds a collection of **ChartPanel** objects containing information about the panels active on the chart.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/chartpanels#property-value)


An **ObservableCollection** of **ChartPanel** objects


## [Syntax](https://developer.ninjatrader.com/docs/desktop/chartpanels#syntax)


`<chartcontrol>.ChartPanels`


## [Examples](https://developer.ninjatrader.com/docs/desktop/chartpanels#examples)
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Based on the image below, there are three ChartPanel objects in the ChartPanels collection, as seen by **ChartPanels.Count** in the code above.


![ChartControl_ChartPanels](https://cdn.sanity.io/images/1hlwceal/production/e617b92f4c2da0945b6852745d6a83c733e787ed-533x432.png)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
   // Print the number of panels currently displayed on the chart
   Print(String.Format("There are {0} panels on the chart", chartControl.ChartPanels.Count));
}
```
