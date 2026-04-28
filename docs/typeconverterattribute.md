# TypeConverterAttribute()

Source: https://developer.ninjatrader.com/docs/desktop/typeconverterattribute

---

# TypeConverterAttribute()


## [Definition](https://developer.ninjatrader.com/docs/desktop/typeconverterattribute#definition)


Binds an object or property to a specific TypeConverter implementation.  This is commonly used to customize property descriptors on the NinjaTrader property grid.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


- If you are looking to extend behavior of an Indicator or Strategy (e.g., values of one property influence another), you must implement either an [IndicatorBaseTypeConverter](https://developer.ninjatrader.com/docs/desktop/indicatorbaseconverter) or [StrategyBaseTypeConveter](https://developer.ninjatrader.com/docs/desktop/strategybaseconverter).  This is to ensure default property descriptor behavior works as intended.
- For converting types of a specific property, implementing a standard TypeConverter is sufficient
- A working NinjaScript demo can be found through the reference sample on "Using a TypeConverter to Customize Property Grid Behavior"
- The TypeConverterAttribute object is a general purpose attribute made available from the .NET Framework. The information on this page is written to demonstrate how you may use this object within NinjaScript conventions used with the NinjaTrader UI's property grid (e.g., an indicator dialog).  There are more methods and properties that you can learn about from MSDN's [TypeConverterAttribute Class](https://msdn.microsoft.com/en-us/library/system.componentmodel.typeconverterattribute(v=vs.110).aspx) which are NOT covered in this topic; as such there is NO guarantee they will work with the NinjaTrader UI's property grids.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/typeconverterattribute#syntax)


`TypeConverterAttribute(string)`


`TypeConverterAttribute(type)`


## [Examples](https://developer.ninjatrader.com/docs/desktop/typeconverterattribute#examples)


```csharp
// Only applied to this property: can just implement a general TypeConveter
[TypeConverter(typeof(MyCustomBoolConveter))]
public bool CustomBool

// Applied to the entire indicator: must implement an IndicatorBaseTypeConveter
[TypeConverter("NinjaTrader.NinjaScript.Indicators.MyConverter")]
public class MyCustomIndicator : Indicator
{

}

// Applied to the entire strategy: must implement a StrategyBaseTypeConveter
[TypeConverter("NinjaTrader.NinjaScript.Strategies.MyCustomConveter")]
public class MyCustomStrategy : Strategy
{

}
```
