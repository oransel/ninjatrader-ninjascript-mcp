# ShowTransparentPlotsInDataBox

Source: https://developer.ninjatrader.com/docs/desktop/showtransparentplotsindatabox

---

# ShowTransparentPlotsInDataBox


## [Definition](https://developer.ninjatrader.com/docs/desktop/showtransparentplotsindatabox#definition)


Determines if plot(s) values which are set to a **Transparent** brush display in the chart data box. The default behavior is to hide any plots which have been configured as a **Transparent** brush, however this behavior can be changed by setting **ShowTransparentPlotsInDataBox** to true on the indicator.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/showtransparentplotsindatabox#property-value)


This property returns true if transparent indicator plot(s) values display in the chart data box; otherwise, false. Default set to false.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


This property should ONLY be set from the **OnStateChange()** method during **State.SetDefaults** or **State.Configure**.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/showtransparentplotsindatabox#syntax)


`ShowTransparentPlotsInDataBox`


## [Examples](https://developer.ninjatrader.com/docs/desktop/showtransparentplotsindatabox#examples)


```csharp
protected override void OnStateChange()
{
     if (State == State.SetDefaults)
     {
         ShowTransparentPlotsInDataBox = true;
         AddPlot(Brushes.Transparent, "MyPlot");
     }
}
```
