# ArePlotsConfigurable

Source: https://developer.ninjatrader.com/docs/desktop/areplotsconfigurable

---

# ArePlotsConfigurable


## [Definition](https://developer.ninjatrader.com/docs/desktop/areplotsconfigurable#definition)


Determines if the plot(s) used in an indicator are configurable within the indicator dialog window.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/areplotsconfigurable#property-value)


A **bool** which returns true if any indicator plot(s) are configurable; otherwise, false. Default set to true.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/areplotsconfigurable#syntax)


`ArePlotsConfigurable`


## [Examples](https://developer.ninjatrader.com/docs/desktop/areplotsconfigurable#examples)


```csharp
protected override void OnStateChange()
  {
      if (State == State.SetDefaults)
      {
          AddPlot(Brushes.Orange, "SMA");
          ArePlotsConfigurable = false; // Plots are not configurable in the indicator dialog
      }
  }
```
