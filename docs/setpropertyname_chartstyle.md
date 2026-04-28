# SetPropertyName()

Source: https://developer.ninjatrader.com/docs/desktop/setpropertyname_chartstyle

---

# SetPropertyName()


## [Definition](https://developer.ninjatrader.com/docs/desktop/setpropertyname_chartstyle#definition)


Sets a default property name to a custom string to be displayed on the UI.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/setpropertyname_chartstyle#method-return-value)


This method does not return a value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/setpropertyname_chartstyle#syntax)


`SetPropertyName(string propertyName, string displayName)`


## [Method Parameters](https://developer.ninjatrader.com/docs/desktop/setpropertyname_chartstyle#method-parameters)


| --- |
| propertyName | A string representing the property to be renamed. Possible values include:

- **UpBrush**
- **DownBrush**
- **BarWidth**
- **Stroke**
- **Stroke2** |
| displayName | A string representing the desired property name |


## [Examples](https://developer.ninjatrader.com/docs/desktop/setpropertyname_chartstyle#examples)


```csharp
protected override void OnStateChange()
{
   if (State == State.Configure)
   {
       Properties.Remove(Properties.Find("Stroke", true));
       Properties.Remove(Properties.Find("Stroke2", true));

       SetPropertyName("UpBrush", "AdvanceBar");
       SetPropertyName("DownBrush", "DeclineBar");
   }
}
```

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


If you do not wish to use specific properties accessible via **SetPropertyName**(), you will need to remove them from the list via **Properties.Remove**, as shown in the example above.
