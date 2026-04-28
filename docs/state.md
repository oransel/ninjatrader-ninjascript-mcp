# State

Source: https://developer.ninjatrader.com/docs/desktop/state

---

# State


## [Definition](https://developer.ninjatrader.com/docs/desktop/state#definition)


Represents the current progression of the object as it advances from setup, processing data, to termination. These states can be used for setting up or declaring various resources and properties.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


More detailed explanation of various states along with examples can be found in the **OnStateChange()** method section of this help guide. You can also attempt to set a new State using the **SetState()** method.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/state#property-value)


An enum value representing the current state of the object. Possible values are:


| State | Description |
| --- | --- |
| **SetDefaults** | Default values are set (pushed to UI). |
| **Configure** | User the presses the OK or Apply button. |
| **Active** | Object is configured and is ready to receive instructions. |
| **DataLoaded** | All data series have been loaded. |
| **Historical** | Begins to process historical data. |
| **Transition** | Finished processing historical data. |
| **Realtime** | Begins to process realtime data. |
| **Terminated** | Begins to shut down. |


## [Syntax](https://developer.ninjatrader.com/docs/desktop/state#syntax)


`State`


## [Examples](https://developer.ninjatrader.com/docs/desktop/state#examples)


### **Understanding the sequence of States**


```csharp
protected override void OnStateChange()
{
  Print(DateTime.Now + ": Current State is State." + State);
}
```


### **Using State to only process real-time data**


```csharp
protected override void OnBarUpdate()
{
   // only process real-time OnBarUpdate events
   if (State == State.Historical)
     return;

   //rest of logic
}
```
