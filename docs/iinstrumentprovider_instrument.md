# Instrument

Source: https://developer.ninjatrader.com/docs/desktop/iinstrumentprovider_instrument

---

# Instrument


In order for instrument linking to work properly in your Add On, **Instrument** must be created.


## [Examples](https://developer.ninjatrader.com/docs/desktop/iinstrumentprovider_instrument#examples)


```csharp
// IInstrumentProvider membepublic Instrument Instrument
{
     get { return instrument; }
     set
     {
         if (instrument != null)
         {
             // Unsubscribe to subscriptions to previously selected instrument
         }

         if (value != null)
         {
             // Create subscriptions for the newly selected instrument
         }

         instrument = value;

         // Send instrument to other windows linked to the same color
         PropagateInstrumentChange(value);

         // Update the tab header name
         RefreshHeader();
     }
}
```
