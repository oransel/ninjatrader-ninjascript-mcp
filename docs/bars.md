# Bars

Source: https://developer.ninjatrader.com/docs/desktop/bars

---

# Bars


## [Definition](https://developer.ninjatrader.com/docs/desktop/bars#definition)


Represents the data returned from the historical data repository. The Bars object contain several methods and properties for working with bar data.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


The Bars object and its member should NOT be accessed within the [OnStateChange()](https://developer.ninjatrader.com/docs/desktop/onstatechange) method before the State has reached **State.DataLoaded**


## [Additional Access Information](https://developer.ninjatrader.com/docs/desktop/bars#additional-access-information)


Members within the Bars class can be accessed without a null reference check in the OnBarUpdate() event handler. When the OnBarUpdate() event is triggered, there will always be a Bar object which holds the method or property. Should you wish to access these members elsewhere, check for null reference first. e.g. if (Bars != null)


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/bars#methods-and-properties)


| [BarsSinceNewTradingDay](https://developer.ninjatrader.com/docs/desktop/barssincenewtradingday) | Number of bars that have elapsed since the start of the trading day |
| --- | --- |
| [GetAsk()](https://developer.ninjatrader.com/docs/desktop/getask) | Returns the Ask price |
| [GetBar()](https://developer.ninjatrader.com/docs/desktop/getbar) | Returns the bar index based on time |
| [GetBid()](https://developer.ninjatrader.com/docs/desktop/getbid) | Returns the Bid price |
| [GetClose()](https://developer.ninjatrader.com/docs/desktop/getclose) | Returns the closing price |
| [GetDayBar()](https://developer.ninjatrader.com/docs/desktop/getdaybar) | Returns a Bar object that represents a trading day whose properties for open, high, low, close, time and volume can be accessed. |
| [GetHigh()](https://developer.ninjatrader.com/docs/desktop/gethigh) | Returns the High price |
| [GetLow()](https://developer.ninjatrader.com/docs/desktop/getlow) | Returns the Low price |
| [GetOpen()](https://developer.ninjatrader.com/docs/desktop/getopen) | Returns the opening price |
| [GetTime()](https://developer.ninjatrader.com/docs/desktop/gettime) | Returns the time |
| [GetVolume()](https://developer.ninjatrader.com/docs/desktop/getvolume) | Returns the volume |
| [IsFirstBarOfSession](https://developer.ninjatrader.com/docs/desktop/isfirstbarofsession) | Returns true if the bar is the first bar of a session |
| [IsFirstBarOfSessionByIndex()](https://developer.ninjatrader.com/docs/desktop/isfirstbarofsessionbyindex) | Returns true if the bar is the first bar of a session |
| [IsLastBarOfSession](https://developer.ninjatrader.com/docs/desktop/islastbarofsession) | Returns true if the bar is the last bar of a session |
| [IsResetOnNewTradingDay](https://developer.ninjatrader.com/docs/desktop/isresetonnewtradingday) | Returns true if the chart bars should reset on a new trading day |
| [IsTickReplay](https://developer.ninjatrader.com/docs/desktop/istickreplay) | Returns true if the bars are using tick replay |
| [PercentComplete](https://developer.ninjatrader.com/docs/desktop/percentcomplete) | Value indicating the completion percent of a bar |
| [TickCount](https://developer.ninjatrader.com/docs/desktop/tickcount) | Total number of ticks of the current bar |
| [ToChartString()](https://developer.ninjatrader.com/docs/desktop/tochartstring) | Returns the bars series as a string formatted as the series would be displayed in the user interface |
