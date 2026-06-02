# Options

Source: https://developer.ninjatrader.com/docs/desktop/connections_options

---

# Options


## [Definition](https://developer.ninjatrader.com/docs/desktop/connections_options#definition)


The connection's configuration options


## [Properties](https://developer.ninjatrader.com/docs/desktop/connections_options#properties)


| --- |
| ConnectOnStartup | A bool representing if this connection auto connects on startup -- | Name | A string representing the connection's name |
| Provider | A Provider representing the connection's provider |


## [Examples](https://developer.ninjatrader.com/docs/desktop/connections_options#examples)


```csharp
// Example of accessing information on all connected connections
public class MyAddOnTab : NTTabPage
{
    public MyAddOnTab()
    {
        // Print information about all connected connections
        lock (Connection.Connections)
            Connection.Connections.ToList().ForEach(c => NinjaTrader.Code.Output.Process(string.Format("Connection: {0} Provider: {1}", c.Options.Name, c.Options.Provider), PrintTo.OutputTab1));
    }

    // Other required NTTabPage members left out for demonstration purposes. Be sure to add them in your own code.
}
```
