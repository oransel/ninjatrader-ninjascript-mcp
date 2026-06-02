# RearmAlert()

Source: https://developer.ninjatrader.com/docs/desktop/alert_rearmalert

---

# RearmAlert()


## [Definition](https://developer.ninjatrader.com/docs/desktop/alert_rearmalert#definition)


Rearms an existing alert event by the string "id" parameter created via the [AlertCallback()](https://developer.ninjatrader.com/docs/desktop/alertcallback) method. A NinjaScript generated alert by may need to be rearmed after the alert is triggered depending on the Alert()'s rearmSeconds parameter.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


The NinjaScriptBase has a non-static method implemented with the same name. Please see the [RearmAlert()](https://developer.ninjatrader.com/docs/desktop/rearmalert) method for Indicator or Strategies.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/alert_rearmalert#method-return-value)


This method does not return a value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/alert_rearmalert#syntax)


`NinjaTrader.NinjaScript.Alert.RearmAlert(string id)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/alert_rearmalert#parameters)


| --- |
| id | A unique string id representing an alert id to reset |


## [Examples](https://developer.ninjatrader.com/docs/desktop/alert_rearmalert#examples)


```csharp
if (resetCondition)
{
   NinjaTrader.NinjaScript.Alert.ResetAlertRearmById("someId");
   resetCondition = false;
}
```
