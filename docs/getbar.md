# GetBar()

Source: https://developer.ninjatrader.com/docs/desktop/getbar

---

# GetBar()


## [Definition](https://developer.ninjatrader.com/docs/desktop/getbar#definition)


Returns the first bar that matches the time stamp of the "time" parameter provided.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


If the time parameter provided is older than the first bar in the series, a bar index of 0 is returned. If the time stamp is newer than the last bar in the series, the last absolute bar index is returned.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/getbar#method-return-value)


An **int** value representing an absolute bar index value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/getbar#syntax)


`Bars.GetBar(DateTime time)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/getbar#parameters)


| Parameter | Description |
| --- | --- |
| time | Time stamp to be converted to an absolute bar index |


## [Examples](https://developer.ninjatrader.com/docs/desktop/getbar#examples)


```csharp
// Check that its past 9:45 AM
if (ToTime(Time[0]) >= ToTime(9, 45, 00))
{
    // Calculate the bars ago value for the 9 AM bar for the current day
    int barsAgo = CurrentBar - Bars.GetBar(new DateTime(2006, 12, 18, 9, 0, 0));

    // Print out the 9 AM bar closing price
    Print("The close price on the 9 AM bar was: " + Close[barsAgo].ToString());
}
```
