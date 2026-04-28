# ConnectionStatusUpdate

Source: https://developer.ninjatrader.com/docs/desktop/connectionstatusupdate

---

# ConnectionStatusUpdate


## [Definition](https://developer.ninjatrader.com/docs/desktop/connectionstatusupdate#definition)


**ConnectionStatusUpdate** can be used for subscribing to connection status update events.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Remember to unsubscribe if you are no longer using the subscription.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/connectionstatusupdate#syntax)


`ConnectionStatusUpdate`


## [Examples](https://developer.ninjatrader.com/docs/desktop/connectionstatusupdate#examples)


```csharp
// Example of subscribing/unsubscribing to connection update events from an Add On. The concept can be carried over
// to any NinjaScript object you may be working on.
public class MyAddOnTab : NTTabPage
{
    private Connection connection;
    public MyAddOnTab()
    {
        // Subscribe to connection updates
        Connection.ConnectionStatusUpdate += OnConnectionStatusUpdate;
    }

    // This method is fired on connection status update events
    private void OnConnectionStatusUpdate(object sender, ConnectionStatusEventArgs e)
    {
        // For multi-threading reasons, work with a copy of the ConnectionStatusEventArgs to prevent situations
        // where the ConnectionStatusEventArgs may already be ahead of us while in the middle processing it.
        ConnectionStatusEventArgs eCopy = e;

        // If the Kinetick EOD connection disconnects, do something
        if (eCopy.Connection.Options.Name == "Kinetick - End Of Day (Free)")
        {
            if (eCopy.Status == ConnectionStatus.Disconnected)
                // Do something
        }
    }

    // Called by TabControl when tab is being removed or window is closed
    public override void Cleanup()
    {
        // Make sure to unsubscribe to the connection status subscription
        Connection.ConnectionStatusUpdate -= OnConnectionStatusUpdate;
    }

    // Other required NTTabPage members left out for demonstration purposes. Be sure to add them in your own code.
}
```
