# ConnectOptions

Source: https://developer.ninjatrader.com/docs/desktop/connectoptions

---

# ConnectOptions


## [Definition](https://developer.ninjatrader.com/docs/desktop/connectoptions#definition)


**ConnectOptions** is an abstract class used to configure options for a specific configured [Connection](https://developer.ninjatrader.com/docs/desktop/connection). An instance of **ConnectOptions** can be passed into the **Connection.Connect()** method to initiate a connection, as seen in the example below.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


For a complete, working example of this class in use, download the framework example located on our [Developing AddOns Overview](https://developer.ninjatrader.com/docs/desktop/developing_add_ons).


## [Properties](https://developer.ninjatrader.com/docs/desktop/connectoptions#properties)


Properties accessible from an instance of **ConnectOptions** include:


| --- |
| BrandName | A string representing the provider name |
| CanEnableHds | A bool determining the connection can use NinjaTrader Historical Data Servers. Related properties include **HasHdsAlwaysEnabled** and **IsHdsEnabled** |
| CanManageOrders | A bool determining orders can be managed on the Connection. Related properties include **IsDataProviderOnly** |
| Mode | A **NinjaTrader.Cbi.Mode** object representing the current mode of the connection (**Mode.Live** or **Mode.Simulation**) |
| Name | The user-configured name of the Connection | Provider | The provider configured in the Connection |


## [Examples](https://developer.ninjatrader.com/docs/desktop/connectoptions#examples)


```csharp
// Connecting to a configured connection
private Connection Connect(string connectionName)
{
    // Get the configured account connection by using the string passed into this custom Connect() method
    // We will lock the ConnectOptions collection to avoid in-flight changes causing any issues
    ConnectOptions connectOptions = null;
    lock (Core.Globals.ConnectOptions)
        connectOptions = Core.Globals.ConnectOptions.FirstOrDefault(o => o.Name == connectionName);

    // If connection is not already connected, connect to it
    lock (Connection.Connections)
        if (Connection.Connections.FirstOrDefault(c => c.Options.Name == connectionName) == null)
        {
            Connection connect = Connection.Connect(connectOptions);

            // Only return connection if successfully connected
            if (connect.Status == ConnectionStatus.Connected)
                return connect;
            else
                return null;
        }
}
```
