# ApproxCompare()

Source: https://developer.ninjatrader.com/docs/desktop/approxcompare

---

# ApproxCompare()


## [Definition](https://developer.ninjatrader.com/docs/desktop/approxcompare#definition)


Compares two double or float values for equality or being greater than / less than the compared to value.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Comparing for being greater than / less is done using an epsilon value of 1E19


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/approxcompare#method-return-value)


An **int** value representing the outcome of the comparison. Returns 0 if values are equal, 1 if value1 is greater than value2. -1 if value1 is less than value2.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/approxcompare#syntax)


`this.ApproxCompare(this double double1, double double2)`


`this.ApproxCompare(this float float1, double float2)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/approxcompare#parameters)


| Parameter | Description |
| --- | --- |
| double1 / float1 | First value to compare against (not actually passed in) |
| double2 / float2 | Second passed in value to compare against |

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Main use would be using it for equality comparisons to circumvent running into floating point considerations, value compares for < or > could be usually done more straightforward directly.


## [Examples](https://developer.ninjatrader.com/docs/desktop/approxcompare#examples)


```csharp
// Build the High / Low difference and if 0 sets the indicator main Value series to 0
if ((High[0] - Low[0]).ApproxCompare(0) == 0)
   Value[0] = 0;
```
