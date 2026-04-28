# ToTime()

Source: https://developer.ninjatrader.com/docs/desktop/totime

---

# ToTime()


## [Definition](https://developer.ninjatrader.com/docs/desktop/totime#definition)


Calculates an integer value representing a time.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Integer representation of time is in the format Hmmss where 7:30 AM would be 73000 and 2:15:12 PM would be 141512.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/totime#method-return-value)


An **int** value representing a time structure.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/totime#syntax)


`ToTime(DateTime time)`


`ToTime(int hour, int minute, int second)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/totime#parameters)


| Parameter | Description |
| --- | --- |
| **time** | A DateTime structure to calculate. Note: See also the [Time](https://developer.ninjatrader.com/docs/desktop/time) property. |
| **hour** | An **int** value representing the hour used for the input. |
| **minute** | An **int** value representing the minute used for the input. |
| **second** | An **int** value representing the second used for the input. |

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


NinjaScript uses the .NET DateTime structure which can be complicated for novice programmers. If you are familiar with **C#** you can directly use DateTime structure properties and methods for date and time comparisons; otherwise, use this method and the [ToDay()](https://developer.ninjatrader.com/docs/desktop/today) method.


## [Examples](https://developer.ninjatrader.com/docs/desktop/totime#examples)


```csharp
// Only trade between 7:45 AM and 1:45 PM
if (ToTime(Time[0]) >= 74500 && ToTime(Time[0]) <= 134500)
{
    // Strategy logic goes here
}
```


```csharp
// Store start time as an int variable to be compared
int startTime = ToTime(9, 30, 00); // 93000

// Only trade after 9:30 AM
if (ToTime(Time[0]) >= startTime)
{
    // Strategy logic goes here
}
```
