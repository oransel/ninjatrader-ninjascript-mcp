# Plots

Source: https://developer.ninjatrader.com/docs/desktop/strategy_plots

---

# Plots


Plotting functionality for NinjaScript Strategies is largely identical to the framework for Indicators. Please review the [Plots](https://developer.ninjatrader.com/docs/desktop/plots) / [AddPlot()](https://developer.ninjatrader.com/docs/desktop/addplot) page under the Indicators section.


An overview of the draw or plotting related methods / properties available to NinjaScript Strategies vs. Indicators is listed below -


| Method or Property | Strategy | Indicator |
| --- | --- | --- |
| [AddChartIndicator()](https://developer.ninjatrader.com/docs/desktop/addchartindicator) | ✅ | ✘ |
| [AddLine()](https://developer.ninjatrader.com/docs/desktop/addline) | ✅ | ✅ |
| [AddPlot()](https://developer.ninjatrader.com/docs/desktop/addplot) | ✅ | ✅ |
| [AllowRemovalOfDrawObjects](https://developer.ninjatrader.com/docs/desktop/allowremovalofdrawobjects) | ✅ | ✅ |
| [AreLinesConfigurable](https://developer.ninjatrader.com/docs/desktop/arelinesconfigurable) | ✅ | ✅ |
| [ArePlotsConfigurable](https://developer.ninjatrader.com/docs/desktop/areplotsconfigurable) | ✅ | ✅ |
| [BackBrush](https://developer.ninjatrader.com/docs/desktop/backbrush) | ✅ | ✅ |
| [BackBrushAll](https://developer.ninjatrader.com/docs/desktop/backbrushall) | ✅ | ✅ |
| [BackBrushes](https://developer.ninjatrader.com/docs/desktop/backbrushes) | ✅ | ✅ |
| [BackBrushesAll](https://developer.ninjatrader.com/docs/desktop/backbrushesall) | ✅ | ✅ |
| [BarBrush](https://developer.ninjatrader.com/docs/desktop/barbrush) | ✅ | ✅ |
| [BarBrushes](https://developer.ninjatrader.com/docs/desktop/barbrushes) | ✅ | ✅ |
| [CandleOutlineBrush](https://developer.ninjatrader.com/docs/desktop/candleoutlinebrush) | ✅ | ✅ |
| [CandleOutlineBrushes](https://developer.ninjatrader.com/docs/desktop/candleoutlinebrushes) | ✅ | ✅ |
| [ChartBars](https://developer.ninjatrader.com/docs/desktop/chartbars) | ✅ | ✅ |
| [ChartControl](https://developer.ninjatrader.com/docs/desktop/chartcontrol) | ✅ | ✅ |
| [ChartIndicators[]](https://developer.ninjatrader.com/docs/desktop/chartindicators) | ✅ | ✘ |
| [ChartObjects](https://developer.ninjatrader.com/docs/desktop/chartobjects) | ✘ | ✅ |
| [ChartPanel](https://developer.ninjatrader.com/docs/desktop/chartpanel) | ✅ | ✅ |
| [DisplayInDataBox](https://developer.ninjatrader.com/docs/desktop/displayindatabox) | ✅ | ✅ |
| [Draw.Methods()](https://developer.ninjatrader.com/docs/desktop/drawing) | ✅ | ✅ |
| [DrawHorizontalGridLines](https://developer.ninjatrader.com/docs/desktop/drawhorizontalgridlines) | ✘ | ✅ |
| [DrawObjects](https://developer.ninjatrader.com/docs/desktop/drawobjects) | ✅ | ✅ |
| [DrawOnPricePanel](https://developer.ninjatrader.com/docs/desktop/drawonpricepanel) | ✅ | ✅ |
| [DrawVerticalGridLines](https://developer.ninjatrader.com/docs/desktop/drawverticalgridlines) | ✘ | ✅ |
| [ForceRefresh()](https://developer.ninjatrader.com/docs/desktop/forcerefresh) | ✘ | ✅ |
| [FormatPriceMarker()](https://developer.ninjatrader.com/docs/desktop/formatpricemarker) | ✅ | ✅ |
| [GetValueAt()](https://developer.ninjatrader.com/docs/desktop/getvalueat) | ✅ | ✅ |
| [IsAutoScale](https://developer.ninjatrader.com/docs/desktop/isautoscale) | ✅ | ✅ |
| [IsOverlay](https://developer.ninjatrader.com/docs/desktop/isoverlay) | ✅ | ✅ |
| [IsTradingHoursBreakLineVisible](https://developer.ninjatrader.com/docs/desktop/istradinghoursbreaklinevisible) | ✘ | ✅ |
| [IsValidDataPoint()](https://developer.ninjatrader.com/docs/desktop/isvaliddatapoint) | ✅ | ✅ |
| [Lines[]](https://developer.ninjatrader.com/docs/desktop/lines) | ✅ | ✅ |
| [MaxValue](https://developer.ninjatrader.com/docs/desktop/maxvalue) | ✅ | ✅ |
| [MinValue](https://developer.ninjatrader.com/docs/desktop/minvalue) | ✅ | ✅ |
| [OnCalculateMinMax()](https://developer.ninjatrader.com/docs/desktop/oncalculateminmax) | ✅ | ✅ |
| [OnRender()](https://developer.ninjatrader.com/docs/desktop/onrender) | ✅ | ✅ |
| [OnRenderTargetChanged()](https://developer.ninjatrader.com/docs/desktop/onrendertargetchanged) | ✅ | ✅ |
| [PaintPriceMarkers](https://developer.ninjatrader.com/docs/desktop/paintpricemarkers) | ✘ | ✅ |
| [Panel](https://developer.ninjatrader.com/docs/desktop/panelindex) | ✅ | ✅ |
| [PanelUI](https://developer.ninjatrader.com/docs/desktop/panelui) | ✅ | ✅ |
| [PlotBrushes[]](https://developer.ninjatrader.com/docs/desktop/plotbrushes) | ✅ | ✅ |
| [Plots[]](https://developer.ninjatrader.com/docs/desktop/plots) | ✅ | ✅ |
| [RemoveDrawObject()](https://developer.ninjatrader.com/docs/desktop/removedrawobject) | ✅ | ✅ |
| [RemoveDrawObjects()](https://developer.ninjatrader.com/docs/desktop/removedrawobjects) | ✅ | ✅ |
| [RenderTarget](https://developer.ninjatrader.com/docs/desktop/rendertarget) | ✅ | ✅ |
| [ScaleJustification](https://developer.ninjatrader.com/docs/desktop/scalejustification) | ✅ | ✅ |
| [SetZOrder()](https://developer.ninjatrader.com/docs/desktop/setzorder) | ✅ | ✅ |
| [ShowTransparentPlotsInDataBox](https://developer.ninjatrader.com/docs/desktop/showtransparentplotsindatabox) | ✅ | ✅ |
| [UserControllCollection[]](https://developer.ninjatrader.com/docs/desktop/UserControlCollection) | ✅ | ✅ |
| [ZOrder](https://developer.ninjatrader.com/docs/desktop/chart_zorder) | ✅ | ✅ |
