# MergePolicy

Source: https://developer.ninjatrader.com/docs/desktop/barsrequest_mergepolicy

---

# MergePolicy


## [Definition](https://developer.ninjatrader.com/docs/desktop/barsrequest_mergepolicy#definition)


Determines the merge policy of the bars request.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This property is ONLY applicable to Futures contracts. General information regarding merge policies can be found from the [Market Data Configuration](https://ninjatrader.com/support/helpGuides/nt8/NT%20HelpGuide%20English.html?merge_policy.htm) section. For an Instruments configured merge policy, please see the [MasterInstrument.MergePolicy](https://developer.ninjatrader.com/docs/desktop/mergepolicy) property.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/barsrequest_mergepolicy#property-value)


Represents the MergePolicy used for the bars request.


Possible values are:


| --- |
| DoNotMerge | No merge policy is applied |
| MergeBackAdjusted | Merge policy is applied between contracts along with rollover offsets |
| MergeNonBackAdjusted | Merge policy is applied between contracts without offsets |
| UseGlobalSettings | Uses the value configured from Tools -> Options -> Market Data |
| UseDefault | Uses the default values configured for the [MasterInstrument](https://developer.ninjatrader.com/docs/desktop/masterinstrument) |


## [Syntax](https://developer.ninjatrader.com/docs/desktop/barsrequest_mergepolicy#syntax)


`MergePolicy`


## [Example](https://developer.ninjatrader.com/docs/desktop/barsrequest_mergepolicy#example)


```csharp
// request the last 365 1 day bars
BarsRequest useGlobalRequest = new BarsRequest(Instrument.GetInstrument("ES 09-16"), 365);
useGlobalRequest.BarsPeriod = new BarsPeriod { BarsPeriodType = BarsPeriodType.Day, Value = 1 };

// use the merge policy the user has configured as their global setting
useGlobalRequest.MergePolicy = MergePolicy.UseGlobalSettings;
useGlobalRequest.Request(new Action<barsrequest, errorcode,="" string="">((barsRequest, errorCode, errorMessage) =>{

   Print("bars returned=" + barsRequest.Bars.Count);

}));

// dispose of the bars request if we are done with it
useGlobalRequest.Dispose();
```
