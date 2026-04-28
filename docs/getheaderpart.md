# GetHeaderPart()

Source: https://developer.ninjatrader.com/docs/desktop/getheaderpart

---

# GetHeaderPart()


## [Definition](https://developer.ninjatrader.com/docs/desktop/getheaderpart#definition)


Indicates the tab header name.


## [Examples](https://developer.ninjatrader.com/docs/desktop/getheaderpart#examples)


```csharp
// NTTabPage member. Required for determining the tab header name
protected override string GetHeaderPart(string variable)
{
     // Determine the text for the tab header name
     switch (variable)
     {
         case "@INSTRUMENT": return Instrument == null ? Resource.GuiNewTab : Instrument.MasterInstrument.Name;
         case "@INSTRUMENT_FULL": return Instrument == null ? Resource.GuiNewTab : Instrument.FullName;
     }
     return variable;
}
```
