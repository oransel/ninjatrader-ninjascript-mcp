# Visual Studio Debugging

Source: https://developer.ninjatrader.com/docs/desktop/visual_studio_debugging

---

# Visual Studio Debugging


You can debug your NinjaScript objects using Microsoft Visual Studio. NinjaScript objects are compiled into a single DLL, named "NinjaTrader.Custom.dll." When debugging, a special debug DLL is created for temporary use, with the same name as the release version.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Notes:


- Using the debug DLL can incur a runtime performance impact, so it is recommended to disable Visual Studio debugging and re-compile your scripts when finished. This will replace the debug DLL with the release version.
- The Visual Studio button will work with Visual Studio 2019 or 2022 - if multiple versions are installed, it will start the highest one.


## [Using Visual Studio Debugging](https://developer.ninjatrader.com/docs/desktop/visual_studio_debugging#using-visual-studio-debugging)


- In the NinjaScript Editor, enable "Debug Mode" via the right-click menu, as seen in the image below. After this, compile your scripts to create the debug DLL.


![NS_Editor_5](https://cdn.sanity.io/images/1hlwceal/production/d310c526dac51e20086d8b2600dbb22d478a4c15-900x700.png)


- From the NinjaScript Editor, click on the Visual Studio icon ![NS_Editor_6](https://cdn.sanity.io/images/1hlwceal/production/36b7c4117794260cb3021470cf080b64a4b640ad-28x20.png) from the tool bar, which will automatically load the NinjaTrader.Custom project with your installed version of Visual Studio.
- In Visual Studio, select Debug, then select Attach to Process


![NS_Editor_7](https://cdn.sanity.io/images/1hlwceal/production/118baab5b79e90f3920adca0dc25e0a44e19651e-347x462.png)


- Select NinjaTrader from the list of processes, then select Attach. Be sure the "Attach to" field is set to "Automatic: Managed code" or "Managed code".


![NS_Editor_8](https://cdn.sanity.io/images/1hlwceal/production/d563351a37675eaadf037d7364b38cd26a32ca75-870x586.png)


- Open the NinjaScript source file within Microsoft Visual Studio and set your break point(s)


![NS_Editor_9](https://cdn.sanity.io/images/1hlwceal/production/955a1f4f25f1eb3bd551ac35e5599a383fd6035c-1201x718.png)


- Run your NinjaScript object in NinjaTrader and it should stop at your break points and all the debugging tools and information should be available to inspect the current state of the code.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


You can also use Visual Studio as editor for your NinjaScript files - for that open the project as in step 2 above and then use Visual Studio for editing and once done save the file (don't run or build the solution then in Visual Studio), preferably with the NinjaScript editor opened still at the same time, so changes would be auto compiled in then.
