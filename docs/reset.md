# Reset()

Source: https://developer.ninjatrader.com/docs/desktop/reset

---

# Reset()


## [Definition](https://developer.ninjatrader.com/docs/desktop/reset#definition)


Resets the internal marker which is used for **IsValidDataPoint()** back to false. Calling the **Reset()** method is unique and can be very powerful for custom indicator development. **Series`<t>`** objects will always contain a value which is assigned, however calling **Reset()** simply means you effectively ignore the value of the current bar for plotting purposes. For calculation purposes you will want to use **IsValidDataPoint()** to ensure you are not calculating off of any reset values assigned by the **Reset()** method.


| --- |
| Series Type | Value after Reset() |
| **Series<`bool`>** | false |
| **Series<`double`>** | 0.00 |
| **Series<`datetime`>** | DateTime.MinValue |
| **Series<`float`>** | 0 |
| **Series<`int`>** | 0 |
| **Series<`long`>** | 0 |
| **Series<`string`>** | null |


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/reset#method-return-value)


This method does not return a value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/reset#syntax)


`Reset()`


`Reset(int barsAgo)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/reset#parameters)


| --- |
| **barsAgo** | An int representing from the current bar the number of historical bars the method will check. If no barsAgo value is supplied, the current bar value will be reset instead (barsAgo 0). |


## [Examples](https://developer.ninjatrader.com/docs/desktop/reset#examples)


```csharp
protected override void OnBarUpdate()
{
    // set MyPlot to Low of current bar minus 1 tick
    MyPlot[0] = Low[0] - (1 * TickSize);

    //reset MyPlot every 10 bars
    if(CurrentBar % 10 == 0)
        MyPlot.Reset();

    // only calculate MyPlot value if it has not be reset
    if(MyPlot.IsValidDataPoint(0))
        Print(CurrentBar + " Value is: " + MyPlot[0]);
}
```
