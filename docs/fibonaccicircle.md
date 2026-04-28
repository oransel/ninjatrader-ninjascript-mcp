# FibonacciCircle

Source: https://developer.ninjatrader.com/docs/desktop/fibonaccicircle

---

# FibonacciCircle


## [Definition](https://developer.ninjatrader.com/docs/desktop/fibonaccicircle#definition)


Represents an interface that exposes information regarding a Fibonacci Circle **IDrawingTool**.


## [Methods and Properties](https://developer.ninjatrader.com/docs/desktop/fibonaccicircle#methods-and-properties)


| Parameter | Description |
| --- | --- |
| StartAnchor | An IDrawingTool's ChartAnchor representing the starting point of the drawing object |
| EndAnchor | An IDrawingTool's ChartAnchor representing the end point of the drawing object |
| PriceLevels | A collection of prices calculated by the drawing object |
| IsTimePriceDividedSeparately | A bool value which when true determines if the time and price are calculated together as a ratio, or independently |
| IsTextDisplayed | A bool value determining if the draw object should display text on the chart. |


## [Examples](https://developer.ninjatrader.com/docs/desktop/fibonaccicircle#examples)


```csharp
// Instantiate a Fibonacci circle
FibonacciCircle myFibCirc = Draw.FibonacciCircle(this, "tag1", true, 10, Low[10], 0, High[0]);

// Ensure that text is being displayed on the Drawing Object
myFibCirc.IsTextDisplayed = true;
```
