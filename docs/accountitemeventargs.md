# AccountItemEventArgs

Source: https://developer.ninjatrader.com/docs/desktop/accountitemeventargs

---

# AccountItemEventArgs


## [Definition](https://developer.ninjatrader.com/docs/desktop/accountitemeventargs#definition)


**AccountItemEventArgs** contains **Account**-related information to be passed as an argument to the **OnAccountItemUpdate** event.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


For a complete, working example of this class in use, download framework example located on our **Developing AddOns Overview**.


The properties listed below are accessible from an instance of AccountItemEventArgs:


| Account | The Account for which OnAccountItemUpdate() was called |
| --- | --- |
| AccountItem | The **AccountItem** which has updated, resulting in the call to OnAccountItemUpdate() |
| Currency | The currency of the Account in question |
| Time | A DateTime object representing the time at which the change occurred |
| Value | The new value of the updated AccountItems |


## [Example](https://developer.ninjatrader.com/docs/desktop/accountitemeventargs#example)


```csharp
// This method is fired on any change of an AccountItem
private void OnAccountItemUpdate(object sender, AccountItemEventArgs e)
{
    /* Dispatcher.InvokeAsync() is needed for multi-threading considerations. When processing events outside of the UI thread, and we want to
    influence the UI .InvokeAsync() allows us to do so. It can also help prevent the UI thread from locking up on long operations. */
    Dispatcher.InvokeAsync(() =>
    {
        //Print which AccountItem changed, on which account, and the new value, using
        outputBox.AppendText(string.Format("{0}Account: {1}{0}AccountItem: {2}{0}Value: {3}",
            Environment.NewLine,
            e.Account.Name,
            e.AccountItem,
            e.Value));
    });
}
```
