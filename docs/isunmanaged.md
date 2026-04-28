# IsUnmanaged

Source: https://developer.ninjatrader.com/docs/desktop/isunmanaged

---

# IsUnmanaged


## [Definition](https://developer.ninjatrader.com/docs/desktop/isunmanaged#definition)


Determines if the strategy will be using Unmanaged order methods.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Unmanaged order methods and **Managed order methods** cannot be used interchangeably. When **IsUnmanaged** is set to true, calling managed order methods such as **EnterLong()**, **SetStopLoss()**, etc., will generate an error which will be displayed on the **Log tab** of the Control Center.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/isunmanaged#property-value)


This property returns true if the strategy will use Unmanaged order methods; otherwise, false. Default is set to false.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


Warning: This property should ONLY be set from the **OnStateChange()** method during **State.SetDefaults** or **State.Configure**.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/isunmanaged#syntax)


`IsUnmanaged`


## [Examples](https://developer.ninjatrader.com/docs/desktop/isunmanaged#examples)


```csharp
protected override void OnStateChange()
{
    if (State == State.SetDefaults)
    {
        // Use Unmanaged order methods
        IsUnmanaged = true;
    }
}
```
