# GetCurrentBidVolume()

Source: https://developer.ninjatrader.com/docs/desktop/getcurrentbidvolume

---

# GetCurrentBidVolume()


## [Definition](https://developer.ninjatrader.com/docs/desktop/getcurrentbidvolume#definition)


Returns the current real-time bid volume.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


- When accessed during **State.Historical**, the [Volume](https://developer.ninjatrader.com/docs/desktop/volume) of the evaluated bar series is substituted. To access historical Bid Volumes, please see [Developing for Tick Replay](https://developer.ninjatrader.com/docs/desktop/developing_for_tick_replay).
- The **GetCurrentBidVolume()** method runs on the bar series currently updating determined by the **BarsInProgress** property. For [multi-instrument](https://developer.ninjatrader.com/docs/desktop/multi_time_frame_instruments) scripts, an additional int "barsSeriesIndex" parameter can be supplied which forces the method to run on a supplementary bar series.


## [MethoReturn Value](https://developer.ninjatrader.com/docs/desktop/getcurrentbidvolume#methoreturn-value)


A long value representing the current bid volume.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/getcurrentbidvolume#syntax)


`GetCurrentBidVolume()`


`GetCurrentBidVolume(int barsSeriesIndex)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/getcurrentbidvolume#parameters)


| Parameter | Description |
| --- | --- |
| **barsSeriesIndex** | An **int** value determining the bar series the method runs. Note: This optional parameter is reserved for multi-instrument scripts |


## [Examples](https://developer.ninjatrader.com/docs/desktop/getcurrentbidvolume#examples)


```csharp
protected override void OnBarUpdate()
{
   long currentBidVolume = GetCurrentBidVolume();
   Print("The Current Bid volume is: " + currentBidVolume);
   //The Current Bid volume is: 158
}
```


```csharp
protected override void OnStateChange()
{
   if (State == State.SetDefaults)
   {
     Name = "Examples Indicator";
   }
   if (State == State.Configure)
   {
     //Add MSFT as our additional data series
     AddDataSeries("MSFT", BarsPeriodType.Minute, 1);
   }
}
```


```csharp
protected override void OnBarUpdate()
{
   if(BarsInProgress == 0)
   {
     long currentBidVolume = GetCurrentBidVolume(0);
     Print("The Current Bid volume is: " + currentBidVolume);
     //The Current Bid volume is: 346
   }

   if(BarsInProgress == 1)

   {

     long msftBidVolume = GetCurrentBidVolume(1);

     Print("MSFT's Current Bid volume is: " + msftBidVolume);

     //MSFT's Current Bid volume is: 1548

   }
```
