# CloseStrategy()

Source: https://developer.ninjatrader.com/docs/desktop/closestrategy

---

# CloseStrategy()


## [Definition](https://developer.ninjatrader.com/docs/desktop/closestrategy#definition)


Cancels all working orders, closes any existing positions, and finally disables the strategy. This behavior can also be overridden for a given strategy if desired.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


- If you choose to override this method using custom logic, the default behavior of the **CloseStrategy()** method will NOT be executed. For this reason, it is suggested to call the base implementation of **CloseStrategy()** method within the virtual override to ensure that the strategy is terminated as designed, otherwise it is your responsibility to correctly manage any working orders or positions.
- **CloseStrategy()** will work of the current strategy position and will not factor in any [StartBehavior](https://developer.ninjatrader.com/docs/desktop/startbehavior) setting, i.e. calling **CloseStrategy()** while the script is in a virtual historical position could result in an unwanted position.
- The default **CloseStrategy()** handling will be applied to all series of a MultiSeries NinjaScript strategy.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/closestrategy#method-return-value)


This method does not return a value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/closestrategy#syntax)


`CloseStrategy(string signalName)`
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


This method can only be called before the [State](https://developer.ninjatrader.com/docs/desktop/state) has reached [State.Terminated](https://developer.ninjatrader.com/docs/desktop/state) and after the [State](https://developer.ninjatrader.com/docs/desktop/state) reaches [State.Realtime](https://developer.ninjatrader.com/docs/desktop/state).


You may choose to override this method using the following syntax:


```csharp
public override void CloseStrategy(string signalName)
{
}
```


## [Parameters](https://developer.ninjatrader.com/docs/desktop/closestrategy#parameters)


| --- |
| **signalName** | The signal name which will be used to identify the closing order. If no signal name exists or is null, "Close" will be substituted instead. |


## [Examples](https://developer.ninjatrader.com/docs/desktop/closestrategy#examples)


```csharp
DateTime StartTime = new DateTime();
protected override void OnStateChange()
{
   if (State == State.SetDefaults)
   {
     Name = "ExampleStrategy";
   }

   else if (State == State.Transition)
     StartTime = Core.Globals.Now;
}

protected override void OnBarUpdate()
{
   // if we're still in position 45 minutes after the start time, close strategy
   if(Position.MarketPosition != MarketPosition.Flat && Time[0] >= StartTime.AddMinutes(45))
     CloseStrategy("My Custom Close");
}
```


### Overriding the Default CloseStrategy logic


```csharp
public override void CloseStrategy(string signalName)
{
   Print("Executing Custom Close Logic");
   // custom close logic
   // call default close action
   base.CloseStrategy(signalName);
}
```
