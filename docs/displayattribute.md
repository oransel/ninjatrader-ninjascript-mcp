# DisplayAttribute

Source: https://developer.ninjatrader.com/docs/desktop/displayattribute

---

# DisplayAttribute


## [Definition](https://developer.ninjatrader.com/docs/desktop/displayattribute#definition)


Determines how the following declared property display on the NinjaTrader UI's property grid.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


The DisplayAttribute object is a general purpose attribute made available from the .NET Framework. The information on this page is written to demonstrate how you may use this object within NinjaScript conventions used with the NinjaTrader UI's property grid (e.g., an indicator dialog). There are more methods and properties that you can learn about from MSDN's [DisplayAttribute Class](https://developer.ninjatrader.com/docs/desktop/displayattribute) which are NOT covered in this topic; as such there is NO guarantee they will work with the NinjaTrader UI's property grids.


## [Syntax](https://developer.ninjatrader.com/docs/desktop/displayattribute#syntax)


`[Display(Name=string)]`


`[Display(Description=string)]`


`[Display(GroupName=string)]`


`[Display(Order=int)]`
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FWarning.3bcf24ba.svg&w=64&q=75)

## Warning


The "Name" parameter MUST be unique for each property of a particular object. Sharing the same Name can have undesirable consequences on various features of the property grid.


## [Parameters](https://developer.ninjatrader.com/docs/desktop/displayattribute#parameters)


| --- |
| Name | A string which sets the text used to display the property on the UI |
| Description | A string which sets the tool tip used to describe the property from the UI Note: Expandable properties will NOT display a tool tip (e.g., **[SimpleFont](https://developer.ninjatrader.com/docs/desktop/simplefont)**, **[Stroke](https://developer.ninjatrader.com/docs/desktop/stroke_class)**, or any custom component which are a type of an ExpandableObjectConverter) |
| GroupName | A string which sets a name that is used to group various properties in the UI. If no GroupName is specified, properties will be listed in the generic "Parameters" section. |
| Order | An int which sets the sequence the property is categorized in relation to other properties in the UI. |

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Tips:


- Multiple named parameters can be written separated by a comma during a single declaration as demonstrated in the example below.
- You may have noticed the default NinjaTrader types such as indicators or strategies use a **ResourceType = typeof(Custom.Resource)** property in the DisplayAttribute. This is done for localization purposes, so the default NinjaTrader UI translates to other supported international languages, but is not required for your custom NinjaScript types. The ResourceType property can be safely ignored and left out in your custom development.


## [Examples](https://developer.ninjatrader.com/docs/desktop/displayattribute#examples)


```csharp
#region Properties
// set how the property displays from the UI property grid
[Display(Name="My Period", Order=1, GroupName="My Parameters")]
public int MyPeriod
{ get; set; }
// #endregion
```
