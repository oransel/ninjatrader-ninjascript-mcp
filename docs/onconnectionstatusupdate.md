# OnConnectionStatusUpdate()

Source: https://developer.ninjatrader.com/docs/desktop/onconnectionstatusupdate

---

# OnConnectionStatusUpdate()


## [Definition](https://developer.ninjatrader.com/docs/desktop/onconnectionstatusupdate#definition)


An event driven method used which is called for every change in connection status.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/onconnectionstatusupdate#method-return-value)


This method does not return a value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/onconnectionstatusupdate#syntax)


You must override the method in your indicator with the following syntax:


**protected override void OnConnectionStatusUpdate(ConnectionStatusEventArgs connectionStatusUpdate)**


## [Method Parameters](https://developer.ninjatrader.com/docs/desktop/onconnectionstatusupdate#method-parameters)


| --- |
| **connectionStatusUpdate** | A **[ConnectionStatusEventArgs](https://developer.ninjatrader.com/docs/desktop/connectionstatuseventargs)** object representing the most recent update in connection. |
| **Status** | Represents the status of the key adapter functionality. If the adapter supports live orders it will set Status to Disconnected when its order system is not connected. |
| **PriceStatus** | Represents the status of the price feed. |


## [Examples](https://developer.ninjatrader.com/docs/desktop/onconnectionstatusupdate#examples)


```csharp
protected override void OnConnectionStatusUpdate(ConnectionStatusEventArgs connectionStatusUpdate)
{
   if(connectionStatusUpdate.Status == ConnectionStatus.Connected)
   {
     Print("Connected for orders at " + DateTime.Now);
   }

   else if(connectionStatusUpdate.Status == ConnectionStatus.ConnectionLost)
   {
     Print("Connection for orders lost at: " + DateTime.Now);
   }
}
```


```csharp
protected override void OnConnectionStatusUpdate(ConnectionStatusEventArgs connectionStatusUpdate)

{

   if(connectionStatusUpdate.PriceStatus == ConnectionStatus.Connected)

   {

     Print("Connected to price feed at " + DateTime.Now);

   }

   else if(connectionStatusUpdate.PriceStatus == ConnectionStatus.ConnectionLost)

   {

     Print("Connection to price feed lost at: " + DateTime.Now);

   }

}
```
