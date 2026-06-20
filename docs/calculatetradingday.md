# CalculateTradingDay()

Source: https://developer.ninjatrader.com/docs/desktop/calculatetradingday

---

# CalculateTradingDay()


## [Definition](https://developer.ninjatrader.com/docs/desktop/calculatetradingday#definition)


Calculates the trading date of the time value passed in as the **timeLocal** argument. This method may need to be used before you can accurately determine various session properties such as [ActualSessionBegin](https://developer.ninjatrader.com/docs/desktop/actualsessionbegin) or [ActualTradingDayEndLocal](https://developer.ninjatrader.com/docs/desktop/actualtradingdayendlocal), etc. **CalculateTradingDay()** also checks the local date/time against the exchange's current date/time to ensure that the script is in sync with the exchange's current day.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


Warning: This method is resource intensive and should ONLY be reserved for situations when calculations would be limited to a few specific use cases.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/calculatetradingday#property-value)


This method does not return a value.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/calculatetradingday#parameters)


| --- |
| **timeLocal** | The DateTime value used to calculate the trading day. |
| **includesEndTimeStamp** | A bool determining if a timestamp of <`n`>:00 should fall into the current session. (e.g., used for time based intraday series such as minute or second). |


## [Syntax](https://developer.ninjatrader.com/docs/desktop/calculatetradingday#syntax)


`<sessioniterator>.CalculateTradingDay(DateTime timeLocal, bool includesEndTimeStamp)`


## [Examples](https://developer.ninjatrader.com/docs/desktop/calculatetradingday#examples)


```csharp
protected override void OnDataPoint(Bars bars, double open, double high, double low, double close, DateTime time, long volume, bool isBar, double bid, double ask)
{
   // build the bars type session iterator from the bars object provided
   if (SessionIterator == null)
     SessionIterator = new SessionIterator(bars);
 
   // calculate the trading day of the time value provided
   SessionIterator.CalculateTradingDay(time, false);
 
   // add a new bar using the sessions exchanges date
   AddBar(bars, open, high, low, close, SessionIterator.ActualTradingDayExchange, volume);
}
```
