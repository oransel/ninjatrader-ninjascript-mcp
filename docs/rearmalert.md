# RearmAlert()

Source: https://developer.ninjatrader.com/docs/desktop/rearmalert

---

# RearmAlert()


## [Definition](https://developer.ninjatrader.com/docs/desktop/rearmalert#definition)


Rearms an alert created via the **Alert()** method.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


A NinjaScript generated alert may need to be rearmed after the alert is triggered depending on the **Alert()** method's **rearmSeconds** parameter.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/rearmalert#method-return-value)


This method does not return a value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/rearmalert#syntax)


`RearmAlert(string id)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/rearmalert#parameters)


| Parameter | Description |
| --- | --- |
| id | A unique string id representing an alert id to rearm |


## [Examples](https://developer.ninjatrader.com/docs/desktop/rearmalert#examples)


```csharp
protected override void OnBarUpdate()
{
   //rearms "myAlert" on each new trading session
   if(Bars.IsFirstBarOfSession)
     RearmAlert("myAlert");
}
```
