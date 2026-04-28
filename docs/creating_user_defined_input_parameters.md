# Creating User Defined Input Parameters

Source: https://developer.ninjatrader.com/docs/desktop/creating_user_defined_input_parameters

---

# Creating User Defined Input Parameters


You can create user defined input parameters for both **NinjaScript** Indicators and Strategies. Although user defined input parameters can be specified as part of the initial set up of **NinjaScript** Indicator or Strategies using the Wizard you may have a requirement to add new parameters at a later point in your development process. To create these parameters you will need to edit your **NinjaScript** code and follow these steps.


- Open your **NinjaScript** file.
- Inside of the `if (State == State.SetDefaults)` statement, assign a value to the variable for your parameter.


```csharp
Period = 5;
```

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This is also where you set the default value for your parameter.
- Scroll down to the bottom of the editor and expand the minimized "Properties" section by clicking on the + sign on the left.
- Use the following template code for each parameter you wish to create. Please note that the type (**int**, **double**, etc.) will differ depending on what type of variable you wish to create.


```csharp
[Range(1, int.MaxValue)]
[NinjaScriptProperty]
[Display(Name="Period", Description="Numbers of bars used for calculations", Order=1, GroupName="Parameters")]
public int Period
{ get; set; }
```
- To specify lower and upper bounds, you would modify `[Range(1, int.MaxValue)]`. For example:


```csharp
// No upper bound, lower bound of 1
[Range(1, int.MaxValue)]
// No lower bound, upper bound of 100
[Range(int.MinValue, 100)]
// No lower or upper bound
[Range(int.MinValue, int.MaxValue)]
```
- Use the "Description" field to provide a brief description of what the parameter does.
- Pay attention to this line as the object type will vary depending on the type of parameter you wish to make:


```csharp
public int Period
```
- Now, wherever in your code you want to call the user-definable parameter, just use **Period**.


```csharp
if (SMA(Period)[0] > SMA(Period)[1])
     // Do something
```
