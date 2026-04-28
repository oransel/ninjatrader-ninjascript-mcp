# SetZOrder

Source: https://developer.ninjatrader.com/docs/desktop/setzorder

---

# SetZOrder


## [Definition](https://developer.ninjatrader.com/docs/desktop/setzorder#definition)


Used to assign a unique identifier representing the index in which chart objects are drawn on the chart's Z-axis (front to back ordering). Objects with a higher **ZOrder** are drawn first.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


- To check on which **ZOrder** index the object gets drawn use the [ZOrder](https://developer.ninjatrader.com/docs/desktop/chart_zorder) property.
- Assigning specific **ZOrder** indices to draw at should be done once the [State](https://developer.ninjatrader.com/docs/desktop/onstatechange) has reached **State.Historical**.
- If you want to draw your object behind the bars, assign to use index -1 (like in the example below).
- If you want to draw your object topmost, assign to use index **int.MaxValue**.
- Any levels in between can be directly assigned, the starting / default levels used by NinjaTrader can be seen [here](https://developer.ninjatrader.com/docs/desktop/chart_zorder).
- You can see the highest **ZOrder** currently in a chart with code such our second example below - setting higher values than this value will result in the **ZOrder** to be set to this value, so this can be thought of as the current 'top'.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/setzorder#method-return-value)


This method does not return a value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/setzorder#syntax)


`SetZOrder(int DesiredZOrderLevel)`


## [Examples](https://developer.ninjatrader.com/docs/desktop/setzorder#examples)


```csharp
protected override void OnStateChange()
{
   if (State == State.Historical)
   {
       // Make sure our object plots behind the chart bars
       SetZOrder(-1);
   }
}
```


```csharp
protected override void OnRender(ChartControl cc, ChartScale cs)
{
   Print(ChartPanel.ChartObjects.Max(co => co.ZOrder));
}
```
