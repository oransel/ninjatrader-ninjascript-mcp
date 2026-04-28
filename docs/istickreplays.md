# IsTickReplays

Source: https://developer.ninjatrader.com/docs/desktop/istickreplays

---

# IsTickReplays


## [Definition](https://developer.ninjatrader.com/docs/desktop/istickreplays#definition)


Indicates the specified bar series is using Tick Replay. Please see the help guide topic on using [Tick Replay](https://ninjatrader.com/support/helpGuides/nt8/?tick_replay.htm) for general information on this mode.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


For a primary series, the Tick Replay option must be configured from the UI before a NinjaScript object can take use of this property. The setting on the Chart's Data Series menu will always take precedence for an object series which already exists on the user's chart.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


This property should NOT be accessed within the **OnStateChange()** method before the State has reached **State.DataLoaded**.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/istickreplays#property-value)


A **bool[]** when true, indicates the specified [BarsArray](https://developer.ninjatrader.com/docs/desktop/barsarray) is setup to run Tick Replay; otherwise false. Default value is false.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/istickreplays#syntax)


`IsTickReplays[int idx]`


## [Examples](https://developer.ninjatrader.com/docs/desktop/istickreplays#examples)


```csharp
protected override void OnStateChange()
{
    if(State == State.SetDefaults)
    {
        Name = "Examples Indicator";
    }

    else if (State == State.Configure)
    {
        AddDataSeries("AAPL", BarsPeriodType.Minute, 1);
    }
    else if (State == Data.Loaded)
    {
        // IsTickReplays[0] = true;
        // Programmatically setting this option here for Primary [0] does not have any effect
        // Primary series must be configured from UI

        // It is not possible to combine Tick Replay series and non Tick Replay series in a single chart or script
        // The assignment below would not be necessary if the primary series were set to True via the UI
        // IsTickReplays[1] = true;
    }
}

protected override void OnBarUpdate()
{
    //Print out the current bars series name and tick replays setting on start up
    if (CurrentBar == 0)
        Print(BarsArray[BarsInProgress].ToChartString() + " " + IsTickReplays[BarsInProgress]);
}
```
