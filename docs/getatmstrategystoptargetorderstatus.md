# GetAtmStrategyStopTargetOrderStatus()

Source: https://developer.ninjatrader.com/docs/desktop/getatmstrategystoptargetorderstatus

---

# GetAtmStrategyStopTargetOrderStatus()


## [Definition](https://developer.ninjatrader.com/docs/desktop/getatmstrategystoptargetorderstatus#definition)


Gets the current order state(s) of the specified stop or target order of a still-active ATM strategy.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Notes:


- If the method can't find the specified order(s), an empty array is returned.
- A specified stop or target within an ATM strategy can actually hold multiple orders. For example, if your ATM strategy submits a stop and target and you receive multiple partial fills on entry with a delay of a few seconds or more between entry fills, the ATM strategy will submit stop and target orders for each partial fill all with the same price and order type.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/getatmstrategystoptargetorderstatus#method-return-value)


A string[,] multi-dimensional array holding three dimensions that represent average fill price, filled amount and **order state**. The length (number of elements) represents the number of orders that represent the specified name.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/getatmstrategystoptargetorderstatus#syntax)


`GetAtmStrategyStopTargetOrderStatus(string orderName, string atmStrategyId)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/getatmstrategystoptargetorderstatus#parameters)


| --- |
| **orderName** | The order name such as "Stop1" or "Target2" |
| **atmStrategyId** | The unique identifier for the ATM strategy |


## [Examples](https://developer.ninjatrader.com/docs/desktop/getatmstrategystoptargetorderstatus#examples)


```csharp
protected override void OnBarUpdate()
{
     string[,] orders = GetAtmStrategyStopTargetOrderStatus("Target1", "idValue");

     // Check length to ensure that returned array holds order information
     if (orders.Length > 0)
     {
         for (int i = 0; i < orders.GetLength(0); i++)
         {
               Print("Average fill price is " + orders[i, 0].ToString());
               Print("Filled amount is " + orders[i, 1].ToString());
               Print("Current state is " + orders[i, 2].ToString());
         }
     }
}
```
