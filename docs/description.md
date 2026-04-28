# Description

Source: https://developer.ninjatrader.com/docs/desktop/description

---

# Description


## [Definition](https://developer.ninjatrader.com/docs/desktop/description#definition)


Text which is used on the UI's information box to be displayed to a user when configuring a **NinjaScript** object.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/description#method-return-value)


A **string** value representing text used to describe the object.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


Warning: This property should ONLY be set from the **OnStateChange()** method during **State.SetDefaults** or **State.Configure**.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/description#syntax)


`Description`


## [Examples](https://developer.ninjatrader.com/docs/desktop/description#examples)


```csharp
protected override void OnStateChange()
{
   if (State == State.SetDefaults)
   {
     Name = "Examples Indicator";
     Description = @"An indicator used to demonstrate various NinjaScript methods and properties";
   }
}
```
