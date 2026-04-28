# SendMail()

Source: https://developer.ninjatrader.com/docs/desktop/sendmail

---

# SendMail()


## [Definition](https://developer.ninjatrader.com/docs/desktop/sendmail#definition)


Sends an email message through the default email sharing service.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Notes:


- This method can only be called once the **State** has reached **State.Realtime**. Calls to this method in any other State will be silently ignored (in contrast to the implementation for **AddOns**).
- You MUST configure an email account as a default "Mail" Share Service from the **General Options**.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/sendmail#method-return-value)


This method does not return a value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/sendmail#syntax)


`SendMail(string to, string subject, string text)`
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


If mail is not received, please check the `Log` tab of the control center for any specific errors which could be related to delivering the message.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/sendmail#parameters)


| Parameter | Description |
| --- | --- |
| **to** | The email recipient |
| **subject** | Subject line of email |
| **text** | Message body of email |


## [Examples](https://developer.ninjatrader.com/docs/desktop/sendmail#examples)


```csharp
// Generates an email message
SendMail("customer@winners.com", "Trade Alert", "Buy ES");
```
