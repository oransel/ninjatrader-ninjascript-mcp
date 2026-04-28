# GetBarIdxByX()

Source: https://developer.ninjatrader.com/docs/desktop/getbaridxbyx

---

# GetBarIdxByX()


## [Definition](https://developer.ninjatrader.com/docs/desktop/getbaridxbyx#definition)


Returns the **ChartBars** index value at a specified x-coordinate relative to the ChartControl.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/getbaridxbyx#method-return-value)


An **int** value representing the bar index.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/getbaridxbyx#syntax)


`ChartBars.GetBarIdxByX(ChartControl chartControl, int x)`


## [Method Parameters](https://developer.ninjatrader.com/docs/desktop/getbaridxbyx#method-parameters)


| --- |
| **chartControl** | The **ChartControl** object used to determine the chart's time axis |
| **x** | The x-coordinate used to find a bar index value |


## [Examples](https://developer.ninjatrader.com/docs/desktop/getbaridxbyx#examples)


```csharp
protected override void OnRender(ChartControl chartControl, ChartScale chartScale)
{
   // get the users mouse down point and convert to device pixels for DPI accuracy
   int mousePoint = chartControl.MouseDownPoint.X.ConvertToHorizontalPixels(chartControl.PresentationSource);

   // convert mouse point to bar index
   int barIdx = ChartBars.GetBarIdxByX(chartControl, mousePoint);

   Print("User clicked on Bar #" + barIdx);
}
```
