# PropagateInstrumentChange()

Source: https://developer.ninjatrader.com/docs/desktop/propagateinstrumentchange

---

# PropagateInstrumentChange()


## [Definition](https://developer.ninjatrader.com/docs/desktop/propagateinstrumentchange#definition)


In an **NTWindow**, **PropagateInstrumentChange()** sends an Instrument to other windows with the same Instrument Linking color configured.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


- A public Instrument property must be defined in order to use **PropagateInstrumentChange()**, as in the example below.
- A public Instrument property must be defined in order to use **PropagateInstrumentChange()**, as in the example below.
- For a complete, working example of this class in use, download framework example located on our [Developing AddOns Overview](https://developer.ninjatrader.com/docs/desktop/developing_add_ons).


## [Examples](https://developer.ninjatrader.com/docs/desktop/propagateinstrumentchange#examples)


```csharp
// IInstrumentProvider member. Required if you want to use the instrument link mechanism on an NTWindow.
public Cbi.Instrument Instrument
{
   get { return instrument; }
   set
   {
       // Process logic related to switching instruments, such as:
       // Unsubscribe to subscriptions to old instruments...
       // Subscribe for the new instrument...
       // Change the value displayed in an Instrument Selector in the NTWindow...
       // Update the tab header name on AddOnFramework to be the same name as the new instrument...
       // etc...

       // Send instrument to other windows linked to the same color
       PropagateInstrumentChange(value);
   }
}
```
