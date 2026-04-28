# Export Problems

Source: https://developer.ninjatrader.com/docs/desktop/export_problems

---

# Export Problems


If you are having difficulties exporting **NinjaScript** it could be due to one of the following reasons:
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


If you receive the above error, you will need to compile your **NinjaScript** error-free before you can export. To see if your **NinjaScript** file is error free, open the **NinjaScript Editor** (Tool > Edit **NinjaScript**) and press F5 to compile. If you are trying to check a **NinjaScript Strategy** created from the **Strategy Wizard** you can do the same by finishing the wizard and seeing if you receive the “Strategy successfully generated” message.


If you receive any errors when compiling you will need to address them before exporting.


![Export_Problems_1](https://cdn.sanity.io/images/1hlwceal/production/6ff750b558605494ade20bd949ddf252bf484377-398x137.png)


If you are able to compile without errors and still experience exporting difficulties like the one above, check to see if you receive an error similar to this in the Control Center logs:


> "3/6/2014 9:25:30 AM|2|4|Error compiling export assembly: C:\Users\NinjaTrader\Documents\NinjaTrader 8\bin\Custom\Indicator\MyCustomIndicator.cs(42,18) : error CS0118: **NinjaTrader.Indicator.SMA** is a type but is used like a variable"
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


This error may have a different error code and message depending on which variant of .NET you have installed. An error message indicative of this issue would include an indicator name without quotation marks.


If you experience this error, please follow this procedure:


- Take note of which indicator is referenced by the error. In the above example, it is the **SMA**
- Go to your **NinjaScript Export** utility. (Tools > Export > **NinjaScript**...)
- After press "add" select “System indicators” from the "Type" drop down
- Add the indicator that was referenced in the error to the export list along with your custom **NinjaScript** by pressing the > button
- Press the “Export” button to create your **NinjaScript Archive File**. If you receive the same error again, repeat this procedure until you add all the referenced system indicators and are able to successfully export your custom **NinjaScript**.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


If the indicator referenced in the error is another custom indicator you will need to follow the same procedure to add the custom indicator.
