# Export

Source: https://developer.ninjatrader.com/docs/desktop/export

---

# Export


You can export **NinjaScript** for others to import in several formats:


- **Source files** - **NinjaScript** source files that can be imported and edited by others.
- **Assemblies** - A compiled assembly (DLL) of **NinjaScript** that "hides" your source code. This can be further [protected by SecureTeam's Agile.NET](https://developer.ninjatrader.com/docs/desktop/protection_dll_security) to prevent theft of your intellectual property.


## [Exporting NinjaScript as Source Files](https://developer.ninjatrader.com/docs/desktop/export#exporting-ninjascript-as-source-files)


You may want to provide other **NinjaTrader** users with source files of your **NinjaScript** in a format where they are able to view and edit them.


- From the Control Center window select the menu Tools > Export > **NinjaScript**... to open the "Export **NinjaScript**" dialog window.
- Press "add".
- Use the "Type" drop down to filter available **NinjaScript** types.
- Select all of the files that you want to export and press the "OK" button.
- A list of all files that will be exported will be shown.
- Press the "Export" button to export the selected files.
- A file dialog will open where you can choose the location your zip export file will be created in. Per default the **NinjaScript Archive File** (.zip) file will be created in **My Documents<ninjatrader folder="">\bin\Custom\ExportNinjaScript**.
- The file can be [imported](https://developer.ninjatrader.com/docs/desktop/import) by another **NinjaTrader** application on a different PC.


![exportninjascript_1](https://cdn.sanity.io/images/1hlwceal/production/897005539711e34af1234300862cfc0818f34e2f-399x358.png)


## [Exporting NinjaScript as Assembly](https://developer.ninjatrader.com/docs/desktop/export#exporting-ninjascript-as-assembly)
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


You may want to provide other **NinjaTrader** users with access to your proprietary indicators or strategies in a secure format preventing them from being able to see your proprietary source code. You can do this by exporting your **NinjaScript** indicators as a compiled **Microsoft .NET** assembly (DLL) file.


- From the Control Center window select the menu Tools > Export > **NinjaScript**... to open the "Export **NinjaScript**" dialog window.
- Select the option "Export as compiled assembly".
- You can optionally select "Protect compiled assembly" (For information on protection see the "[Protection/DLL Security](https://developer.ninjatrader.com/docs/desktop/protection_dll_security)" page).
- Press "add".
- Use the "Type" drop down to filter available **NinjaScript** types.
- Select all of the files that you want to export and press the "OK" button.
- A list of all files that will be exported will be shown.
- Optionally enter information that describes the assembly in the "Product" and "Version" fields.
- Press the "Export" button to export the selected files.
- A file dialog will open where you can choose the location your zip export file will be created in. Per default the **NinjaScript Archive File** (.zip) file will be created in **My Documents<ninjatrader folder="">\bin\Custom\ExportNinjaScript**.
- The file can be imported by another **NinjaTrader** application on a different PC.


![exportninjascript_3.png](https://cdn.sanity.io/images/1hlwceal/production/2fc37dc822f98ca167ae618b43ae02c53a86c98f-399x358.png)
