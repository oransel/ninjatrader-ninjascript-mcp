# Removing draw objects from the chart

Source: https://developer.ninjatrader.com/docs/desktop/removing_draw_objects_from_the_chart

---

# Removing draw objects from the chart


Drawing objects can be used for a number of different purposes, like keeping track of where a strategy has its entry point, profit target, and stop loss. If a strategy draws an object(s) for every trade it takes, the chart could quickly become cluttered. This sample will show how to remove the objects that aren't necessary anymore.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This is a real-time only strategy. Please view this strategy on a real-time data connection or the Simulated Data Feed.


## [Key concepts in this example](https://developer.ninjatrader.com/docs/desktop/removing_draw_objects_from_the_chart#key-concepts-in-this-example)


- Drawing lines at the price where the orders are that extend for the duration of the trade
- Removing those lines when the trade is over


## [Important related documentation](https://developer.ninjatrader.com/docs/desktop/removing_draw_objects_from_the_chart#important-related-documentation)


- [Draw](https://developer.ninjatrader.com/docs/desktop/drawing)
- [Line()](https://developer.ninjatrader.com/docs/desktop/line)
- [RemoveDrawObject()](https://developer.ninjatrader.com/docs/desktop/removedrawobject)
- [RemoveDrawObjects()](https://developer.ninjatrader.com/docs/desktop/removedrawobjects)
- [CrossAbove()](https://developer.ninjatrader.com/docs/desktop/crossabove)
- [CrossBelow()](https://developer.ninjatrader.com/docs/desktop/crossbelow)


## [Import instructions](https://developer.ninjatrader.com/docs/desktop/removing_draw_objects_from_the_chart#import-instructions)


- Download the file contained in this Help Guide topic to your PC desktop
- From the Control Center window, select the menu Tools > Import > NinjaScript
- Select the downloaded file


[SampleRemoveDrawObjects_NT8.zip](https://ninjatrader.com/support/helpGuides/nt8/samples/SampleRemoveDrawObjects_NT8.zip)
