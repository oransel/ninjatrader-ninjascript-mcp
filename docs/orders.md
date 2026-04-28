# Orders

Source: https://developer.ninjatrader.com/docs/desktop/orders

---

# Orders


## [Definition](https://developer.ninjatrader.com/docs/desktop/orders#definition)


A collection of Order objects generated for the specified account


## [Property Value](https://developer.ninjatrader.com/docs/desktop/orders#property-value)


An **Collection** of Order objects
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Please keep in mind that orders placed when in **State.Historical** are not submitted live to an account.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/orders#syntax)


`<account>.Orders`


## [Examples](https://developer.ninjatrader.com/docs/desktop/orders#examples)


```csharp
private Account myAccount;

protected override void OnStateChange()
{
   if (State == State.SetDefaults)
   {
       // Initialize myAccount
   }
}

private void OnAccountItemUpdate(object sender, AccountItemEventArgs e)
{
   // Print the name and order action of each order processed on the account
   foreach (Order order in myAccount.Orders)
   {
       Print(String.Format("Order placed: {0} - {1}", order.Name, order.OrderAction));
   }
}
```
