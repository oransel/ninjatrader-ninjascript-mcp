# IsDefault

Source: https://developer.ninjatrader.com/docs/desktop/isdefault

---

# IsDefault


## [Definition](https://developer.ninjatrader.com/docs/desktop/isdefault#definition)


Sets the default Share Service used when the type of sharing service is selected.


For example, if you are using two different email adapters, you may set one to be the default when the user selects the email sharing service. Setting this property as the default would only apply to any email adapters and would not apply to any other types of sharing services which have their own respective default adapter.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/isdefault#property-value)


A bool value that represents if the current adapter is default Share Service used for that type of sharing service.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


This property should ONLY be set from the **OnStateChange()** method during **State.SetDefaults**.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/isdefault#syntax)


`Default`


## [Examples](https://developer.ninjatrader.com/docs/desktop/isdefault#examples)


```csharp
protected override void OnStateChange()
{
    if (State == State.SetDefaults)
    {
        Default        = false;
    }
}
```
