# BarsSinceEntryExecution()

Source: https://developer.ninjatrader.com/docs/desktop/barssinceentryexecution

---

# BarsSinceEntryExecution()


## [Definition](https://developer.ninjatrader.com/docs/desktop/barssinceentryexecution#definition)


Returns the number of bars that have elapsed since the last entry. When a signal name is provided, the number of bars that have elapsed since that last specific entry will be returned.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/barssinceentryexecution#method-return-value)


An **int** value that represents a number of bars. A value of -1 will be returned if a previous entry does not exist.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/barssinceentryexecution#syntax)


`BarsSinceEntryExecution()`


`BarsSinceEntryExecution(string signalName)`


The following method signature should be used when working with [multi-time frame and instrument strategies](https://developer.ninjatrader.com/docs/desktop/multi_time_frame_instruments):


`BarsSinceEntryExecution(int barsInProgressIndex, string signalName, int entryExecutionsAgo)`
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


When working with a multi-series strategy the BarsSinceEntryExecution() will return you the elapsed bars as determined by the first Bars object for the instrument specified by the barsInProgressIndex.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/barssinceentryexecution#parameters)


| --- |
| signalName | The signal name of an entry order specified in an order entry method. |
| barsInProgressIndex | The index of the Bars object the entry order was submitted against. Note: See the [BarsInProgress](https://developer.ninjatrader.com/docs/desktop/barsinprogress) property. |
| entryExecutionsAgo | Number of entry executions ago. Pass in 0 for the number of bars since the last entry execution. |


## [Examples](https://developer.ninjatrader.com/docs/desktop/barssinceentryexecution#examples)


```csharp
protected override void OnBarUpdate()
{
    if (CurrentBar < BarsRequiredToTrade)
        return;

    // Only enter if at least 10 bars has passed since our last entry
    if ((BarsSinceEntryExecution() > 10 || BarsSinceEntryExecution() == -1) && CrossAbove(SMA(10), SMA(20), 1))
        EnterLong();
}
```
