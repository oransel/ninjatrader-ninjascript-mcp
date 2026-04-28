# Plots

Source: https://developer.ninjatrader.com/docs/desktop/plots

---

# Plots


## [Definition](https://developer.ninjatrader.com/docs/desktop/plots#definition)


A collection holding all of the Plot objects that define their visualization characteristics.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/plots#property-value)


A collection of Plot objects.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/plots#syntax)


`Plots**[int index]`
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


The example code below will change the color of an entire plot series. See [PlotBrushes](https://developer.ninjatrader.com/docs/desktop/plotbrushes) for information on changing only specific segments of a plot instead.


## [Examples](https://developer.ninjatrader.com/docs/desktop/plots#examples)


```csharp
protected override void OnStateChange()
{
   if(State == State.SetDefaults)
   {
       Name = "Examples Indicator";
       // Lines are added to the Lines collection in order
       AddPlot(Brushes.Orange, "Plot1"); // Stored in Plots[0]
       AddPlot(Brushes.Blue, "Plot2");   // Stored in Plots[1]
     }
}

// Dynamically change the primary plot's color based on the indicator value
protected override void OnBarUpdate()
{
   if (Value[0] > 70)
   {
     Plots[0].Brush = Brushes.Blue;
     Plots[0].Width = 2;
   }
   else
   {
     Plots[0].Brush = Brushes.Red;
     Plots[0].Width = 2;
   }
}
```
