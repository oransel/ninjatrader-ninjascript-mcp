# Getting indicator values from a specified time

Source: https://developer.ninjatrader.com/docs/desktop/getting-indicator-values-from-a-specified-time

---

# Getting indicator values from a specified time


## [Getting indicator values from a specified time](https://developer.ninjatrader.com/docs/desktop/getting-indicator-values-from-a-specified-time#getting-indicator-values-from-a-specified-time)


Sometimes, you may want to access a value from a historical point in time, but have not kept track of the value to make this readily available. With **NinjaScript**, it is possible to pick a bar based on time to access that value. **GetBar()** returns the number of bars ago that holds the same timestamp of the time you request. This sample demonstrates how to get an indicator value from 9:30AM of the previous trading day.


## [Key concepts in this example](https://developer.ninjatrader.com/docs/desktop/getting-indicator-values-from-a-specified-time#key-concepts-in-this-example)


- Obtaining a Simple Moving Average value from a specific time by referencing the bar number for that time.


## [Important related documentation](https://developer.ninjatrader.com/docs/desktop/getting-indicator-values-from-a-specified-time#important-related-documentation)


- [GetBar()](https://developer.ninjatrader.com/docs/desktop/getbar)
- [Draw.Line()](https://developer.ninjatrader.com/docs/desktop/draw_line)
- [Time](https://developer.ninjatrader.com/docs/desktop/time)
- [Sessions](https://developer.ninjatrader.com/docs/desktop/tradinghours_sessions)
- [DateTime](https://learn.microsoft.com/en-us/dotnet/api/system.datetime?view=netframework-4.8)


## [Import instructions](https://developer.ninjatrader.com/docs/desktop/getting-indicator-values-from-a-specified-time#import-instructions)


- Download the file contained in this Help Guide topic to your PC desktop.
- From the Control Center window, select the menu Tools > Import > NinjaScript.
- Select the downloaded file.


[SampleGetBar_NT8.zip](https://ninjatrader.com/support/helpGuides/nt8/samples/SampleGetBar_NT8.zip)
