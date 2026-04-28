# How do I resolve NinjaScript Programming Errors?

Source: https://developer.ninjatrader.com/docs/desktop/how_do_i_resolve_ninjascript_programming_errors

---

# How do I resolve NinjaScript Programming Errors?


You may come across various situations where your **NinjaScript** files will not compile. This can include situations such as:


- You are trying to import a **NinjaScript Archive File** and you receive an error such as "You have custom **NinjaScript** files on your PC that have programming errors..."
- You are new to **NinjaScript** development and somehow your files will no longer compile


Because importing **NinjaScript** files requires compilation of your entire **NinjaScript** library you will first need to resolve the errors to allow for a successful compilation.


## [1st Step in Resolving Errors](https://developer.ninjatrader.com/docs/desktop/how_do_i_resolve_ninjascript_programming_errors#1st-step-in-resolving-errors)


- Backup **NinjaScript** files (Tools > Export > Backup File, ensure that "NinjaScript Files" is checked and then press the "Export" button).
- Open the **NinjaScript Editor** via the menu New > **NinjaScript Editor**.
- Press the "F5" key on your keyboard to compile your **NinjaScript** library or right click in the window and click "Compile". A list of errors will appear at the bottom of the **NinjaScript Editor** along with the file name where each error is located.
- Determine if you no longer need the **NinjaScript** file with the errors. If you no longer need it, skip to step 9.
- Double click on the error message to open the **NinjaScript** with the errors. Try to resolve the error and recompile by pressing the "F5" key.
- If the error still exists in this file, "comment out" some or all of the content in the **OnBarUpdate()** method and recompile by pressing the "F5" key.
- If errors still exist in this file, "comment out" some or all of the content in the **OnStateChange()** method and recompile by pressing the "F5" key.
- If errors still exist in this file, "comment out" any properties that in the "Properties" region that may be causing the problems and recompile by pressing the "F5" key.
- If errors still exist in this file, try to remove the file from compilation or delete the file (See "To remove or delete the erroneous file" instructions below).
- If another **NinjaScript** file references a file you wish to delete, open the file that references the file you wish to delete and "comment out" or delete the reference.
- Repeat steps 2 through 10 for every **NinjaScript** that still has errors.


## [To remove or delete the erroneous file](https://developer.ninjatrader.com/docs/desktop/how_do_i_resolve_ninjascript_programming_errors#to-remove-or-delete-the-erroneous-file)


With **NinjaTrader 8**, we now have the option to remove a file from compilation but not delete it.


This means all your code is intact but is not compiled so it will not produce errors. This also means the item is not available for use until you add it back into compilation.


- Open the **NinjaScript Editor** via the menu New > **NinjaScript Editor**.
- Highlight the **NinjaScript** file you wish to prevent from being compiled, Right click on it and click "Exclude from Compilation".
- If another **NinjaScript** file references the file you wish to delete, you must first remove the reference to the file you wish to delete, see step 10 above.
- You also have the option to completely delete the file as well, this is the same process as above except you would select "Remove" instead.


## [2nd Step in Resolving Errors](https://developer.ninjatrader.com/docs/desktop/how_do_i_resolve_ninjascript_programming_errors#2nd-step-in-resolving-errors)


If the above procedure does not resolve all errors, you may need to reinstall **NinjaTrader**.


- Backup **NinjaScript** files (Tools > Export > Backup File, ensure that "NinjaScript Files" is checked and then press the "Export" button).
- Shut down **NinjaTrader**.
- Uninstall **NinjaTrader** from the windows Control Panel Add/Remove Programs.
- Manually delete or move the folder **My Documents\NinjaTrader 8**.
- Reinstall the latest version of **NinjaTrader** from our website.
