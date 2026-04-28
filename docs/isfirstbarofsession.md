# IsFirstBarOfSession

Source: https://developer.ninjatrader.com/docs/desktop/isfirstbarofsession

---

# IsFirstBarOfSession


## [Definition](https://developer.ninjatrader.com/docs/desktop/isfirstbarofsession#definition)


Indicates if the current bar processing is the first bar updated in a trading session.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This property always returns true on the very first bar processed (i.e., **CurrentBar** == 0). The represented time of the bar will NOT necessarily be equal to the trading hours start time (e.g., if you request 50 1-minute bars at 11:50:00 AM, the first bar processed of the session would be 11:00:00 AM). Loading a data series based on "dates" (Days or custom range) ensures that the first bar processed matches hours defined by the session template.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/isfirstbarofsession#property-value)


This property returns true if the bar is the first processed in a session; otherwise, false. This property is read-only.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


This property will always return false on non-intraday bar periods (e.g., Day, Month, etc). For checking for new non-intraday bar updates, please see [IsFirstTickOfBar](https://developer.ninjatrader.com/docs/desktop/isfirsttickofbar).


## [Syntax](https://developer.ninjatrader.com/docs/desktop/isfirstbarofsession#syntax)


`Bars.IsFirstBarOfSession`
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


For checking at a specified bar index, please see [IsFirstBarOfSessionByIndex()](https://developer.ninjatrader.com/docs/desktop/isfirstbarofsessionbyindex).


## [Examples](https://developer.ninjatrader.com/docs/desktop/isfirstbarofsession#examples)


```csharp
protected override void OnBarUpdate()
{
    // Print the current bar number of the first bar processed for each session on a chart
    if (Bars.IsFirstBarOfSession)
        Print(string.Format("Bar number {0} was the first bar processed of the session at {1}.", CurrentBar, Time[0]));
}
```
