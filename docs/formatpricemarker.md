# FormatPriceMarker()

Source: https://developer.ninjatrader.com/docs/desktop/formatpricemarker

---

# FormatPriceMarker()


## [Definition](https://developer.ninjatrader.com/docs/desktop/formatpricemarker#definition)


Used to override the default string format of a NinjaScript's price marker values.


## [Method Return Value](https://developer.ninjatrader.com/docs/desktop/formatpricemarker#method-return-value)


A **virtual** string which is overridden from the default price marker value.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/formatpricemarker#syntax)


You must override the method in your indicator with the following syntax:


**public override string FormatPriceMarker(double price)**


## [Parameters](https://developer.ninjatrader.com/docs/desktop/formatpricemarker#parameters)


| --- |
| price | A **double** value representing the value to be overridden. |


## [Tip](https://developer.ninjatrader.com/docs/desktop/formatpricemarker#tip)


Tip: Standard Numeric Format Strings examples can be found on Microsoft's Developer Network ([MSDN article](https://msdn.microsoft.com/en-us/library/dwhawy9k%28v=vs.110%29.aspx)).


## [Examples](https://developer.ninjatrader.com/docs/desktop/formatpricemarker#examples)


```csharp
// FormatPriceMarker method of a custom indicator
public override string FormatPriceMarker(double price)
{
     // Formats price marker values to 4 decimal places
     return price.ToString("N4");
}

protected override void OnBarUpdate()
{
   // overriding FormatPriceMarker will ensure display of 4 decimal places
   MyPlot[0] = (Close[0] + Open[0] * .0025);
}
```
