# Plotting from within a NinjaScript Strategy

Source: https://developer.ninjatrader.com/docs/desktop/plotting_from_within_a_ninjascript_strategy

---

# Plotting from within a NinjaScript Strategy


When running a strategy on a chart you may find the need to plot values onto a chart. If these values are internal strategy calculations that are difficult to migrate to an indicator, you can use the following technique to achieve a plot.


With **NinjaTrader 8** we introduced strategy plots which provide the ability for a strategy to render its own plots. These plots must be specific to a single panel just like indicators. If you need to have strategy plots on more than a single panel then please use the technique seen in the attached sample. You can find documentation on the standard methods for plotting in the **Indicator** help guide section, although the documents are for indicators the plotting items are shared between indicators and strategies.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


Important related documentation:


- [Plotting from a strategy with Indicator plot methods](https://developer.ninjatrader.com/docs/desktop/addplot)


## [Import instructions](https://developer.ninjatrader.com/docs/desktop/plotting_from_within_a_ninjascript_strategy#import-instructions)


- Download the file contained in this Help Guide topic to your PC desktop.
- From the Control Center window, select the menu **Tools** > **Import** > **NinjaScript**.
- Select the downloaded file.


[SampleStrategyPlot_NT8.zip](https://ninjatrader.com/support/helpGuides/nt8/samples/SampleStrategyPlot_NT8.zip)
