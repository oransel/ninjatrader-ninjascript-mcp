# ISeries

Source: https://developer.ninjatrader.com/docs/desktop/iseriest

---

# ISeries


## [Definition](https://developer.ninjatrader.com/docs/desktop/iseriest#definition)


**ISeries** is an interface that is implemented by all NinjaScript classes that manage historical data as an **ISeries`<double>`** (Open, High, Low, Close, etc), used for indicator input, and other object data. Please see the help guide article on [Working with Price Series](https://developer.ninjatrader.com/docs/desktop/working_with_price_series) for a basic overview on how to access this information.


## [Types of ISeries](https://developer.ninjatrader.com/docs/desktop/iseriest#types-of-iseries)


| [Series<`t`>](https://developer.ninjatrader.com/docs/desktop/seriest) | Represents a generic custom data structure for custom development |
| --- | --- |
| [PriceSeries](https://developer.ninjatrader.com/docs/desktop/priceseries) | Historical price data structured as an **ISeries`<double>`** interface (Close[0], High[0], Low[0], etc) |
| [TimeSeries](https://developer.ninjatrader.com/docs/desktop/timeseries) | Historical time stamps structured as an **ISeries<`datetime`>** interface (Time[0]) |
| [VolumeSeries](https://developer.ninjatrader.com/docs/desktop/volumeseries) | Historical volume data structured as an **ISeries`<double>`** interface (Volume[0]) |


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/iseriest#methods-and-properties)


| --- |
| [GetValueAt()](https://developer.ninjatrader.com/docs/desktop/getvalueat) | Returns the underlying input value at a specified bar index value. |
| [IsValidDataPoint()](https://developer.ninjatrader.com/docs/desktop/isvaliddatapoint) | Indicates if the specified input is set at a barsAgo value relative to the current bar. |
| [IsValidDataPointAt()](https://developer.ninjatrader.com/docs/desktop/isvaliddatapointat) | Indicates if the specified input is set at a specified bar index value. |
| [Count](https://developer.ninjatrader.com/docs/desktop/count) | Return the number total number of values in the **ISeries** array |

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Tips: (see examples below)


- By specifying a parameter of type **ISeries`<double>`**, you can then pass in an array of closing prices, an indicator, or a user defined data series.
- When working with **ISeries`<double>`** objects in your code you may come across situations where you are not sure if the value being accessed is a valid value or just a "placeholder" value. To check if you are using valid values for your logic calculations that have been explicitly set, please use **.IsValidDataPoint(int barsAgo)** to check.


## [Examples](https://developer.ninjatrader.com/docs/desktop/iseriest#examples)


### Using **ISeries** as a method parameter


```csharp
private double DoubleTheValue(ISeries`<double>` priceData)
{
    return priceData[0] * 2;
}

protected override void OnBarUpdate()
{
    Print(DoubleTheValue(Close));
    Print(DoubleTheValue(SMA(20)));
}
```


### Checking **ISeries** value before accessing


```csharp
protected override void OnBarUpdate()
{
    if (Input.IsValidDataPoint(0))
        Plot0[0] = Input[0];
}
```
