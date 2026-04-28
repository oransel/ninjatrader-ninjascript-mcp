# RemoveDrawObject()

Source: https://developer.ninjatrader.com/docs/desktop/removedrawobject

---

# RemoveDrawObject()


## [Definition](https://developer.ninjatrader.com/docs/desktop/removedrawobject#definition)


Removes a draw object from the chart based on its tag value.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This method will ONLY remove DrawObjects which were created by a NinjaScript object. User drawn objects CANNOT be removed from via NinjaScript.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/removedrawobject#method-return-value)


This method does not return a value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/removedrawobject#syntax)


`RemoveDrawObject(string tag)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/removedrawobject#parameters)


| Parameter | Description |
| --- | --- |
| **tag** | A user defined unique id used to reference the draw object. For example, if you pass in a value of "myTag", each time this tag is used, the same draw object is modified. If unique tags are used each time, a new draw object will be created each time. |


## [Examples](https://developer.ninjatrader.com/docs/desktop/removedrawobject#examples)


```csharp
// Removes a draw object with the tag "tag1"**
RemoveDrawObject("tag1");
```
