# OnWindowDestroyed()

Source: https://developer.ninjatrader.com/docs/desktop/onwindowdestroyed

---

# OnWindowDestroyed()


## [Definition](https://developer.ninjatrader.com/docs/desktop/onwindowdestroyed#definition)


This method is called whenever a new **NTWindow** is destroyed. It will be called in the thread of that window. A window is destroyed either by the user closing the window, closing a workspace, or on a shut down of NinjaTrader.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This method will also be called on a recompile of the NinjaTrader.Custom project (e.g., when you compile an indicator, strategy, or add-on)


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/onwindowdestroyed#method-return-value)


This method does not return a value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/onwindowdestroyed#syntax)


`OnWindowDestroyed(Window window)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/onwindowdestroyed#parameters)


| **Parameter** | **Description** |
| --- | --- |
| **window** | A Window object which is being removed from the workspace |


## [Examples](https://developer.ninjatrader.com/docs/desktop/onwindowdestroyed#examples)


```csharp
public class MyWindowAddOn : AddOnBase
{
    private NTMenuItem myMenuItem;
    private NTMenuItem existingMenuItem;

    protected override void OnStateChange()
    {
        if (State == State.SetDefaults)
        {
            Description = "Our custom MyWindow add on";
            Name = "MyWindow";
        }
    }

    // Will be called as a new NTWindow is destroyed. It will be called in the thread of that window
    protected override void OnWindowDestroyed(Window window)
    {
        if (myMenuItem != null && window is ControlCenter)
        {
            if (existingMenuItem != null && existingMenuItem.Items.Contains(myMenuItem))
                existingMenuItem.Items.Remove(myMenuItem);

            myMenuItem.Click -= OnMenuItemClick;
            myMenuItem = null;
        }
    }
}
```
