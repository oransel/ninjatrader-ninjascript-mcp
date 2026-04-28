# TimeSeries<datetime>

Source: https://developer.ninjatrader.com/docs/desktop/timeseries

---

# TimeSeries<datetime>


## [Definition](https://developer.ninjatrader.com/docs/desktop/timeseries#definition)


Represents historical time stamps as an **ISeries<`datetime`>** interface which can be used for custom NinjaScript object calculations.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Note: In most cases, you will access the historical time series using a core event handler such as **OnBarUpdate**. For more advanced developers, you may find situations where you wish to access historical time series outside of the core event methods, such as your own custom mouse click. In these advanced scenarios, you may run into situations where the **barsAgo** pointer is not in sync with the current bar, which may cause errors when trying to obtain this information. In those cases, use the **Bars.Get...()** methods with the absolute bar index, e.g., [**Bars.GetTime()**](https://developer.ninjatrader.com/docs/desktop/gettime).


## [Single ISeries<`datetime`>](https://developer.ninjatrader.com/docs/desktop/timeseries#single-iseries%3C-%3E)


| [Time](https://developer.ninjatrader.com/docs/desktop/time) | A collection of historical bar time stamp values. |
| --- | --- |


## [Multi-Time Frame ISeries<`datetime`>](https://developer.ninjatrader.com/docs/desktop/timeseries#multi-time-frame-iseries%3C-%3E)


| [Times](https://developer.ninjatrader.com/docs/desktop/times) | Holds an array of **ISeries<`datetime`>** objects holding historical bar times. |
| --- | --- |
