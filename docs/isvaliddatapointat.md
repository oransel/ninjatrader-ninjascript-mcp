# IsValidDataPointAt()

Source: https://developer.ninjatrader.com/docs/desktop/isvaliddatapointat

---

# IsValidDataPointAt()


## [Definition](https://developer.ninjatrader.com/docs/desktop/isvaliddatapointat#definition)


Indicates if the specified input is set at a specified bar index value. Please also see the **[Reset()](https://developer.ninjatrader.com/docs/desktop/reset)** method for more information.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


- If called directly from the instance of the **NinjaScript** object, the value returned corresponds to the Inputs Series (e.g., Close, High, Low, SMA, etc.)
- When checking a **[Bar](https://developer.ninjatrader.com/docs/desktop/bars)** or **[PriceSeries](https://developer.ninjatrader.com/docs/desktop/priceseries)**, **IsValidDataPoint()** returns true as long as the barIndex value falls between 0 and the total count for that series. These are special series which always contain a value set at every slot index for multi-series scripting purposes (e.g., comparing two price series with various session templates, or one series has more ticks than the other)
- For a **[Value](https://developer.ninjatrader.com/docs/desktop/value)** series or custom **[Series<`t`>](https://developer.ninjatrader.com/docs/desktop/seriest)**, **IsValidDataPoint()** returns true or false depending on if you have set a value at that index location


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/isvaliddatapointat#method-return-value)


A bool value, when true indicates that specified data point is set; otherwise false.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


Calling **IsValidDataPointAt()** will only work on a MaximumBarsLookBackInfinite series. Attempting to check **IsValidDataPointAt()** on MaximumBarsLookBack256 series will throw an error. Please check the Log tab of the Control Center.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/isvaliddatapointat#syntax)


`IsValidDataPointAt(int barIndex)`


`ISeries<t>.IsValidDataPointAt(int barIndex)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/isvaliddatapointat#parameters)


| Parameter | Description |
| --- | --- |
| barIndex | An int representing an absolute bar index value |


## [Examples](https://developer.ninjatrader.com/docs/desktop/isvaliddatapointat#examples)


```csharp
protected override void OnBarUpdate()
{
    // only set plot value if hosted indicator is not reset
    if(SMA(20).IsValidDataPointAt(CurrentBar))
        MyPlot[0] = SMA(20)[0];
}
```
