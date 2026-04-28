# CandleOutlineBrushes

Source: https://developer.ninjatrader.com/docs/desktop/candleoutlinebrushes

---

# CandleOutlineBrushes


## [Definition](https://developer.ninjatrader.com/docs/desktop/candleoutlinebrushes#definition)


A collection of historical outline brushes for candlesticks.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/candleoutlinebrushes#property-value)


A brush series type object. Accessing this property via an index value **int barsAgo** returns a [brush](http://msdn.microsoft.com/en-us/library/system.windows.media.brush(v=vs.110).aspx) structure representing the referenced bar's outline color.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This will only return the color of a candlestick outline in which an explicit color overwrite was used. Otherwise it will return null.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/candleoutlinebrushes#syntax)


`CandleOutlineBrushes`


`CandleOutlineBrushes[int barsAgo]`
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


Warning: You may have up to 65,535 unique CandleOutlineBrushes instances, therefore, using [static predefined brushes](https://developer.ninjatrader.com/docs/desktop/working_with_brushes) should be favored. Alternatively, in order to use fewer brushes, please try to cache your custom brushes until a new brush would actually need to be created.


## [Examples](https://developer.ninjatrader.com/docs/desktop/candleoutlinebrushes#examples)


```csharp
// Sets the outline color of the current bar to black.
CandleOutlineBrushes[0] = Brushes.Black;

// Sets the outline color of the previous bar to blue.
CandleOutlineBrushes[1] = Brushes.Blue;
```
