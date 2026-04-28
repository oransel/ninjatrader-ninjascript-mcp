# CandleOutlineBrush

Source: https://developer.ninjatrader.com/docs/desktop/candleoutlinebrush

---

# CandleOutlineBrush


## [Definition](https://developer.ninjatrader.com/docs/desktop/candleoutlinebrush#definition)


Sets the outline Brush of a candlestick.


## [Property Value](https://developer.ninjatrader.com/docs/desktop/candleoutlinebrush#property-value)


A **brush** object that represents the color of this price bar.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/candleoutlinebrush#syntax)


`CandleOutlineBrush`
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


You may have up to 65,535 unique `CandleOutlineBrushes` instances, therefore, using [static predefined brushes](https://developer.ninjatrader.com/docs/desktop/working_with_brushes) should be favored. Alternatively, in order to use fewer brushes, please try to cache your custom brushes until a new brush would actually need to be created.


## [Examples](https://developer.ninjatrader.com/docs/desktop/candleoutlinebrush#examples)


```csharp
// Sets the candle outline color to black
CandleOutlineBrush = Brushes.Black;
```

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


You may have up to 65,535 unique CandleOutlineBrushes instances, therefore, using [static predefined brushes](https://developer.ninjatrader.com/docs/desktop/working_with_brushes) should be favored. Alternatively, in order to use fewer brushes, please try to cache your custom brushes until a new brush would actually need to be created.
