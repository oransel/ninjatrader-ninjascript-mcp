# OnFundamentalData()

Source: https://developer.ninjatrader.com/docs/desktop/onfundamentaldata

---

# OnFundamentalData()


## [Definition](https://developer.ninjatrader.com/docs/desktop/onfundamentaldata#definition)


An event driven method which is called for every change in fundamental data for the underlying instrument.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This method is NOT called on historical data (backtest).


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/onfundamentaldata#method-return-value)


This method does not return a value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/onfundamentaldata#syntax)


You must override the method in your strategy or indicator with the following syntax.


**protected override void OnFundamentalData(FundamentalDataEventArgs fundamentalDataUpdate)**
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


The NinjaScript code wizards can automatically generate the method syntax for you when creating a new script.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/onfundamentaldata#parameters)


| Parameter | Description |
| --- | --- |
| **fundamentalDataUpdate** | [FundamentalDataEventArgs](https://developer.ninjatrader.com/docs/desktop/fundamentaldataeventargs) representing the recent change in fundamental data |


## [Examples](https://developer.ninjatrader.com/docs/desktop/onfundamentaldata#examples)


```csharp
protected override void OnFundamentalData(FundamentalDataEventArgs fundamentalDataUpdate)
{
    // Print some data to the Output window
    if (fundamentalDataUpdate.FundamentalDataType == FundamentalDataType.AverageDailyVolume)
        Print("The current ADV is " + fundamentalDataUpdate.LongValue);
}
```

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


- With [multi-time frame and instrument strategies](https://developer.ninjatrader.com/docs/desktop/multi_time_frame_instruments), OnFundamentalData() will be called for all unique instruments in your strategy. Use the [BarsInProgress](https://developer.ninjatrader.com/docs/desktop/barsinprogress) to filter the OnFundamentalData() method for a specific instrument.
- Do not leave an unused OnFundamentalData() method declared in your NinjaScript object. This will unnecessarily attach a data stream to your script which uses unnecessary CPU cycles.
