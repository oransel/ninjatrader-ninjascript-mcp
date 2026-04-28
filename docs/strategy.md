# Strategy

Source: https://developer.ninjatrader.com/docs/desktop/strategy

---

# Strategy


The methods and properties covered in this section are unique to custom strategy development.


## [In this section](https://developer.ninjatrader.com/docs/desktop/strategy#in-this-section)


| [Strategy Account](https://developer.ninjatrader.com/docs/desktop/account) | Represents the real-world or simulation Account configured for the strategy. |
| --- | --- |
| [AddChartIndicator()](https://developer.ninjatrader.com/docs/desktop/addchartindicator) | Adds an indicator to the strategy only for the purpose of displaying it on a chart. |
| [AddPerformanceMetric()](https://developer.ninjatrader.com/docs/desktop/addperformancemetric) | Adds an instance of custom **Performance Metric** to a strategy used in strategy calculations. |
| [ATM Strategy Methods](https://developer.ninjatrader.com/docs/desktop/atm_strategy_methods) | Adds ATM strategies to manage your position |
| [BarsRequiredToTrade](https://developer.ninjatrader.com/docs/desktop/barsrequiredtotrade) | The number of historical bars required before the strategy starts processing order methods called in the **OnBarUpdate()** method. |
| [BarsSinceEntryExecution()](https://developer.ninjatrader.com/docs/desktop/barssinceentryexecution) | Returns the number of bars that have elapsed since the last specified entry. |
| [BarsSinceExitExecution()](https://developer.ninjatrader.com/docs/desktop/barssinceexitexecution) | Returns the number of bars that have elapsed since the last specified exit. |
| [ChartIndicators](https://developer.ninjatrader.com/docs/desktop/chartindicators) | Contains a collection of Indicators which have been added to the strategy instance using **AddChartIndicator()**. |
| [CloseStrategy()](https://developer.ninjatrader.com/docs/desktop/closestrategy) | Cancels all working orders, closes any existing positions, and finally disables the strategy. |
| [ConnectionLossHandling](https://developer.ninjatrader.com/docs/desktop/connectionlosshandling) | Sets the manner in which your strategy will behave when a connection loss is detected. |
| [DaysToLoad](https://developer.ninjatrader.com/docs/desktop/daystoload) | Determines the number of trading days which will be configured when loading the strategy from the Strategies Grid. |
| [DefaultQuantity](https://developer.ninjatrader.com/docs/desktop/defaultquantity) | An order size variable that can be set either programmatically or overridden via the Strategy that determines the quantity of an entry order. |
| [DisconnectDelaySeconds](https://developer.ninjatrader.com/docs/desktop/disconnectdelayseconds) | Determines the amount of time a disconnect would have to last before **connection loss handling** takes action. |
| [EntriesPerDirection](https://developer.ninjatrader.com/docs/desktop/entriesperdirection) | Determines the maximum number of entries allowed per direction while a position is active based on the **EntryHandling** property. |
| [EntryHandling](https://developer.ninjatrader.com/docs/desktop/entryhandling) | Sets the manner in how entry orders will handle. |
| [Execution](https://developer.ninjatrader.com/docs/desktop/execution) | Represents a read-only interface that exposes information regarding an execution (filled order) resulting from an order and is passed as a parameter in the **OnExecutionUpdate()** method. |
| [ExitOnSessionCloseSeconds](https://developer.ninjatrader.com/docs/desktop/exitonsessioncloseseconds) | The number of seconds before the actual session end time that the "**IsExitOnSessionCloseStrategy**" function will trigger. |
| [IncludeCommission](https://developer.ninjatrader.com/docs/desktop/includecommission) | Determines if the strategy performance results will include commission on a historical backtest. |
| [IncludeTradeHistoryInBacktest](https://developer.ninjatrader.com/docs/desktop/includetradehistoryinbacktest) | Determines if the strategy will save orders, trades, and execution history. |
| [IsAdoptAccountPositionAware](https://developer.ninjatrader.com/docs/desktop/isadoptaccountpositionaware) | Determines if the strategy is programmed in a manner capable of handling real-world account positions. |
| [IsExitOnSessionCloseStrategy](https://developer.ninjatrader.com/docs/desktop/isexitonsessionclosestrategy) | Determines if the strategy will cancel all strategy-generated orders and close all open strategy positions at the close of the session. |
| [IsFillLimitOnTouch](https://developer.ninjatrader.com/docs/desktop/isfilllimitontouch) | Determines if the strategy will use a more liberal fill algorithm for back-testing purposes only. |
| [IsInstantiatedOnEachOptimizationIteration](https://developer.ninjatrader.com/docs/desktop/isinstantiatedoneachoptimizationiteration) | Determines if the strategy should be re-instantiated (re-created) after each optimization run when using the **Strategy Analyzer Optimizer**. |
| [IsInStrategyAnalyzer](https://developer.ninjatrader.com/docs/desktop/isinstategyanalyzer) | Determines if the current **NinjaScript Strategy** is run from a Strategy Analyzer chart. |
| [IsTradingHoursBreakLineVisible](https://developer.ninjatrader.com/docs/desktop/istradinghoursbreaklinevisible) | Plots trading hours break lines on the indicator panel. |
| [IsWaitUntilFlat](https://developer.ninjatrader.com/docs/desktop/iswaituntilflat) | Indicates the strategy is currently waiting until a flat position is detected before submitting live orders. |
| [NumberRestartAttempts](https://developer.ninjatrader.com/docs/desktop/numberrestartattempts) | Determines the maximum number of restart attempts allowed within the last x minutes defined in **RestartsWithinMinutes** when the strategy experiences a connection loss. |
| [OnAccountItemUpdate()](https://developer.ninjatrader.com/docs/desktop/onaccountitemupdate) | An event-driven method used for strategies which is called for each AccountItem update for the account on which the strategy is running. |
| [OnExecutionUpdate()](https://developer.ninjatrader.com/docs/desktop/onexecutionupdate) | An event-driven method which is called on an incoming execution of an order managed by a strategy. |
| [OnOrderTrace()](https://developer.ninjatrader.com/docs/desktop/onordertrace) | An event-driven method used for strategies which will allow you to customize the output of **TraceOrders**. |
| [OnOrderUpdate()](https://developer.ninjatrader.com/docs/desktop/onorderupdate) | An event-driven method which is called each time an order managed by a strategy changes state. |
| [OnPositionUpdate()](https://developer.ninjatrader.com/docs/desktop/onpositionupdate) | An event-driven method which is called each time the position of a strategy changes state. |
| [OptimizationPeriod](https://developer.ninjatrader.com/docs/desktop/optimizationperiod) | Reserved for **Walk-Forward Optimization**, this property determines the number of days used for the "in sample" backtest period for a given strategy. See also **TestPeriod**. |
| [Order](https://developer.ninjatrader.com/docs/desktop/order) | Represents a read-only interface that exposes information regarding an order. |
| [Order Methods](https://developer.ninjatrader.com/docs/desktop/order_methods) | **NinjaScript** provides several approaches you can use for order placement within your **NinjaScript strategy**. |
| [OrderFillResolution](https://developer.ninjatrader.com/docs/desktop/orderfillresolution) | Determines how strategy orders are filled during historical states. |
| [OrderFillResolutionType](https://developer.ninjatrader.com/docs/desktop/orderfillresolutiontype) | Determines the bars type which will be used for historical fill processing. |
| [OrderFillResolutionValue](https://developer.ninjatrader.com/docs/desktop/orderfillresolutionvalue) | Determines the bars period interval value which will be used for historical fill processing. |
| [PerformanceMetrics](https://developer.ninjatrader.com/docs/desktop/performancemetrics) | Holds an array of **PerformanceMetrics** objects that represent custom metrics that can be used for strategy calculations. |
| [Plots](https://developer.ninjatrader.com/docs/desktop/strategy_plots) | A collection holding all of the Plot objects that define their visualization characteristics. |
| [Position](https://developer.ninjatrader.com/docs/desktop/position) | Represents position-related information that pertains to an instance of a strategy. |
| [PositionAccount](https://developer.ninjatrader.com/docs/desktop/positionaccount) | Represents position-related information that pertains to real-world account (live or simulation). |
| [Positions](https://developer.ninjatrader.com/docs/desktop/positions) | Holds an array of **Position** objects that represent positions managed by the strategy. |
| [PositionsAccount](https://developer.ninjatrader.com/docs/desktop/positionsaccount) | Holds an array of **PositionAccount** objects that represent positions managed by the strategy's account. |
| [RealtimeErrorHandling](https://developer.ninjatrader.com/docs/desktop/realtimeerrorhandling) | Defines the behavior of a strategy when a strategy-generated order is returned from the broker's server in a "Rejected" state. |
| [RestartsWithinMinutes](https://developer.ninjatrader.com/docs/desktop/restartswithinminutes) | Determines within how many minutes the strategy will attempt to restart. |
| [SetOrderQuantity](https://developer.ninjatrader.com/docs/desktop/setorderquantity) | Determines how order sizes are calculated for a given strategy. |
| [Slippage](https://developer.ninjatrader.com/docs/desktop/slippage) | Sets the amount of slippage in ticks per execution used in performance calculations during backtests. |
| [StartBehavior](https://developer.ninjatrader.com/docs/desktop/startbehavior) | Sets the start behavior of the strategy. See **Syncing Account Positions** for more information. |
| [StopTargetHandling](https://developer.ninjatrader.com/docs/desktop/stoptargethandling) | Determines how stop and target orders are submitted during an entry order execution. |
| [StrategyBaseConverter](https://developer.ninjatrader.com/docs/desktop/strategybaseconverter) | A custom **TypeConverter** class handling the designed behavior of a strategy's property descriptor collection. |
| [SystemPerformance](https://developer.ninjatrader.com/docs/desktop/systemperformance) | The **SystemPerformance** object holds all trades and trade performance data generated by a strategy. |
| [TestPeriod](https://developer.ninjatrader.com/docs/desktop/testperiod) | Reserved for **Walk-Forward Optimization**, this property determines the number of days used for the "out of sample" backtest period for a given strategy. |
| [TimeInForce](https://developer.ninjatrader.com/docs/desktop/timeinforce) | Sets the time in force property for all orders generated by a strategy. |
| [TraceOrders](https://developer.ninjatrader.com/docs/desktop/traceorders) | Determines if **OnOrderTrace()** would be called for a given strategy. |
| [Trade](https://developer.ninjatrader.com/docs/desktop/trade) | A Trade is a completed buy/sell or sell/buy transaction. It consists of an entry and exit execution. |
| [TradeCollection](https://developer.ninjatrader.com/docs/desktop/tradecollection) | A collection of **Trade** objects. |
| [TradesPerformanceValues](https://developer.ninjatrader.com/docs/desktop/tradesperformancevalues) | Performance values of a **collection** of **Trade** objects. |
| [WaitForOcoClosingBracket](https://developer.ninjatrader.com/docs/desktop/waitforococlosingbracket) | Determines if the strategy will submit both legs of an OCO bracket before submitting the pair to the broker. |
