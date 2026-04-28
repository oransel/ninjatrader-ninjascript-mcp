# GetValueAt()

Source: https://developer.ninjatrader.com/docs/desktop/getvalueat

---

# GetValueAt()


## [Definition](https://developer.ninjatrader.com/docs/desktop/getvalueat#definition)


Returns the underlying input value at a specified bar index value.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/getvalueat#method-return-value)


A double value representing the value at a specified bar.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/getvalueat#syntax)


**GetValueAt**(int barIndex)


**ISeries`<t>`.GetValueAt**(int barIndex)
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


If called directly from the instance of the NinjaScript object, the value which is returned corresponds to the input series the object is running. (e.g., Close, High, Low, SMA, etc.). If you're attempting to obtain another indicator value, you will need to pull this from the calculated indicator Value or Plot:


**SMA(20).GetValueAt(123);** // bar value
**SMA(20).Values[0].GetValueAt(123);** // indicator value
**(Input as Indicator).Values[0].GetValueAt(123)** // passed in indicator value


## [Parameters](https://developer.ninjatrader.com/docs/desktop/getvalueat#parameters)


| Parameter | Description |
| --- | --- |
| **barIndex** | An **int** representing an absolute bar index value |


## [Examples](https://developer.ninjatrader.com/docs/desktop/getvalueat#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
    // make sure there are bars displayed on the chart and the chart control is ready before running
    if (Bars == null || chartControl == null)
        return;

    // loop through all the visible bars on the chart
    for (int i = ChartBars.FromIndex - 1; i >= BarsRequiredToPlot; i--)
    {
        double value = GetValueAt(i);
        Print(string.Format("The value at bar {0} is {1}", i, value));
    }
}
```
