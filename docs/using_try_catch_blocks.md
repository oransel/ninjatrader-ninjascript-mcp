# Using Try-Catch Blocks

Source: https://developer.ninjatrader.com/docs/desktop/using_try_catch_blocks

---

# Using Try-Catch Blocks


Debugging your NinjaScript code can be time consuming and frustrating. When NinjaTrader encounters a run-time exception in your programming logic it will terminate the execution of the script and log the exception to the Control Center Log tab. This in itself can be of value however, there may be times where your script is too large and the exception error message provided is not granular enough. This is where standard C# exception handling using the keywords "try" and "catch" (try-catch block) can be very useful. A try-catch block allows you to encapsulate a section of your code to trap exceptions and write out meaningful information that can help you resolve your run-time errors.


## [Key concepts in this example](https://developer.ninjatrader.com/docs/desktop/using_try_catch_blocks#key-concepts-in-this-example)


- try-catch blocks


## [Important related documentation](https://developer.ninjatrader.com/docs/desktop/using_try_catch_blocks#important-related-documentation)


- [Log()](https://developer.ninjatrader.com/docs/desktop/log)
- [Print()](https://developer.ninjatrader.com/docs/desktop/print)
- [PrintTo()](https://developer.ninjatrader.com/docs/desktop/printto)


## [Import instructions](https://developer.ninjatrader.com/docs/desktop/using_try_catch_blocks#import-instructions)


- Download the file contained in this Help Guide topic to your PC desktop
- From the Control Center window, select the menu Tools > Import > NinjaScript
- Select the downloaded file


[SampleTryCatch_NT8.zip](https://ninjatrader.com/support/helpGuides/nt8/samples/SampleTryCatch_NT8.zip)
