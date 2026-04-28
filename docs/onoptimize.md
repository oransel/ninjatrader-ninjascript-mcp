# OnOptimize()

Source: https://developer.ninjatrader.com/docs/desktop/onoptimize

---

# OnOptimize()


## [Definition](https://developer.ninjatrader.com/docs/desktop/onoptimize#definition)


This method must be overridden in order to optimize a strategy. This method is called once per optimization run (not once per iteration).


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/onoptimize#method-return-value)


This method does not return a value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/onoptimize#syntax)


You must override the method in your Optimizer with the following syntax.


`protected override void OnOptimize() { }`


## [Examples](https://developer.ninjatrader.com/docs/desktop/onoptimize#examples)


```csharp
protected override void OnOptimize()
{
     // If there is no optimization objective, return
     if (Strategies[0].OptimizationParameters.Count == 0)
         return;

     // Optimizer logic
}
```
