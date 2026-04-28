# SupportsAlerts

Source: https://developer.ninjatrader.com/docs/desktop/supportsalerts

---

# SupportsAlerts


## [Definition](https://developer.ninjatrader.com/docs/desktop/supportsalerts#definition)


Determines if the drawing tool can be used for manually configured alerts through the UI.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/supportsalerts#property-value)


A bool which when true determines that user can setup an alert based off this drawing tool; otherwise false.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This property is false by default and MUST be overridden upon initialization to allow for manually configured alerts. You cannot set this during run-time.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/supportsalerts#syntax)


`SupportsAlerts`


You may choose to override this property using the following syntax:


**public override bool SupportsAlerts**


## [Examples](https://developer.ninjatrader.com/docs/desktop/supportsalerts#examples)


```csharp
public override bool SupportsAlerts { get { return true; } }
```
