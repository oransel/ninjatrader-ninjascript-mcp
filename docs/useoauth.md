# UseOAuth

Source: https://developer.ninjatrader.com/docs/desktop/useoauth

---

# UseOAuth


## [Definition](https://developer.ninjatrader.com/docs/desktop/useoauth#definition)


If this property is set to true, a Connect button will appear in the dialogue for configuring the adapter that will call **OnAuthorizeAccount()** when the user clicks it.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/useoauth#property-value)


A bool value determining if the **OnAuthorizeAccount()** method should be called in order to authorize the account to the social service.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


This property should ONLY be set from the **OnStateChange()** method during State.SetDefaults.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/useoauth#syntax)


`UseOAuth`


## [Examples](https://developer.ninjatrader.com/docs/desktop/useoauth#examples)


```csharp
protected override void OnStateChange()
{
   if (State == State.SetDefaults)
   {
      UseOAuth = true;
   }
}
```
