# GetMedian()

Source: https://developer.ninjatrader.com/docs/desktop/getmedian

---

# GetMedian()


## [Definition](https://developer.ninjatrader.com/docs/desktop/getmedian#definition)


Returns the statistical median value of the specified series over the specified look-back period. This method sorts the values of the specified look back period in ascending order and returns the middle value.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


- This method should NOT be confused with **Median** prices defined as (**High** + **Low**) / 2. This method returns the statistical median of a series.
- If an even number is passed as the look-back period, the average of the two middle values in the sorted values will be returned.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/getmedian#method-return-value)


A **double** value representing the median value of the series.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/getmedian#syntax)


`GetMedian(ISeries<double> series, int lookBackPeriod)`


## [Parameters](https://developer.ninjatrader.com/docs/desktop/getmedian#parameters)


| --- |
| **lookBackPeriod** | Number of bars back to include in the calculation |
| **series** | Any **Series<`double`>** type object such as an indicator, **Close**, **High**, **Low**, etc... |


## [Examples](https://developer.ninjatrader.com/docs/desktop/getmedian#examples)


```csharp
protected override void OnBarUpdate()
{  
   // Print the median price of the last 10 open prices
   //(current open price + look back period's 9 open prices before that)
   double openMedian = GetMedian(Open, 9);        
   Print("The median of the last 10 open prices is: " + openMedian);      
}
```
