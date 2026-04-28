# Count

Source: https://developer.ninjatrader.com/docs/desktop/count

---

# Count


## [Definition](https://developer.ninjatrader.com/docs/desktop/count#definition)


The total number of bars or data points.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/count#property-value)


An **int** value representing the total number of bars.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/count#syntax)


`Count`


## [Examples](https://developer.ninjatrader.com/docs/desktop/count#examples)


```csharp
//If there are less than 365 bars on the chart, text indicates how many bars are on the chart
if (Count < 365)
{
  Draw.TextFixed(this, "tag1", "There are " + Count + " bars on the chart", TextPosition.BottomRight);
}
```

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


[CurrentBar](https://developer.ninjatrader.com/docs/desktop/currentbar) value is guaranteed to be <= Count - 1. This is because of the NinjaTrader multi-threaded architecture, the Count value can have additional bars as inflight ticks come in to the system.
