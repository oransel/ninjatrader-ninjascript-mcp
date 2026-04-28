# Referencing the correct bar

Source: https://developer.ninjatrader.com/docs/desktop/referencing_the_correct_bar

---

# Referencing the correct bar


When coding an indicator or strategy it is important to be able to access the intended bars for correct calculations. In **NinjaScript** we are able to access the bars we want through proper use of the bar's indexing.


The bar's indexing is setup in a reverse chronological order. This means "0" refers to the most recent bar, "1" refers to the previous bar, "2" refers to the bar before that one, etc.


For example, if we wanted to subtract the high and low of 10 bars ago from each other we would do this:


```csharp
double value = High[10] - Low[10];
```


Now that we know how the indexing works there are several properties and methods at our disposal that can help us access important keystone bars. The more important ones are [CurrentBar](https://developer.ninjatrader.com/docs/desktop/currentbar) and [BarsSinceNewTradingDay](https://developer.ninjatrader.com/docs/desktop/barssincenewtradingday).


## [CurrentBar](https://developer.ninjatrader.com/docs/desktop/referencing_the_correct_bar#currentbar)


CurrentBar returns an int representing the number of bars existing on the chart. This property is most useful when you want to run calculations from the very beginning of the chart.


For example, if you wanted to find the average high value of the first 10 bars on the chart you could do this:


```csharp
double highValue = 0;
int x = CurrentBar;
while (x > CurrentBar - 10)
{
    highValue += High[x];
    x--;
}
Print("The average high value: " + highValue/10)
```

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


A common mistake in using CurrentBar is using it in the index to access the most recent bar. In this situation, instead of doing something like Close[CurrentBar] you will want to do Close[0].


## [BarsSinceNewTradingDay](https://developer.ninjatrader.com/docs/desktop/referencing_the_correct_bar#barssincenewtradingday)


BarsSinceNewTradingDay is another property that can help you find the first bar of the current trading day. The difference between BarsSinceNewTradingDay and CurrentBar is that BarsSinceNewTradingDay resets its count whenever a new session begins. This means if you use it in an index it will only get you to the beginning of the current session and not any previous sessions.


For example, if you wanted to find the open of the current session you could do this:


```csharp
double openValue = Open[Bars.BarsSinceNewTradingDay];
```


The example used in the discussion about CurrentBar can also be done with Bars.BarsSinceNewTradingDay if you wanted to calculate values based on the current session instead of the start of the chart too.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


If you wish to access values older than 256 bars ago you will need to ensure the [MaximumBarsLookBack](https://developer.ninjatrader.com/docs/desktop/maximumbarslookback) is set to .Infinite.


## [Other Properties and Methods](https://developer.ninjatrader.com/docs/desktop/referencing_the_correct_bar#other-properties-and-methods)


There are also a number of other properties and methods that can be useful in helping you locate the correct bars index to reference. Please take a look at these in the help guide:


- [BarsSinceEntryExecution()](https://developer.ninjatrader.com/docs/desktop/barssinceentryexecution)
- [BarsSinceExitExecution()](https://developer.ninjatrader.com/docs/desktop/barssinceexitexecution)
- [GetBar()](https://developer.ninjatrader.com/docs/desktop/getbar)
- [GetDayBar()](https://developer.ninjatrader.com/docs/desktop/getdaybar)
- [HighestBar()](https://developer.ninjatrader.com/docs/desktop/highestbar)
- [LowestBar()](https://developer.ninjatrader.com/docs/desktop/lowestbar)
- [LRO()](https://developer.ninjatrader.com/docs/desktop/least_recent_occurrence_lro)
- [MRO()](https://developer.ninjatrader.com/docs/desktop/most_recent_occurrence_mro)
