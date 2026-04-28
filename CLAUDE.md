# NinjaTrader Desktop SDK – Knowledge Base

This directory contains a local mirror of the NinjaTrader Desktop SDK
documentation scraped from https://developer.ninjatrader.com/docs/desktop.

Each `.md` file corresponds to one documentation page.

Use this knowledge base to answer questions about NinjaScript, indicators,
strategies, drawing tools, and all other NinjaTrader Desktop SDK APIs.

## Directory Structure

```
├── docs/               ← Main API documentation (1066 files)
├── education/          ← Educational resources
└── best-practices/     ← NinjaScript coding guidelines
```

## Key Documentation Areas (in docs/)

### Core Concepts
- `onbarupdate.md` - Main calculation method
- `onstatechange.md` - Lifecycle management
- `calculate.md` - Calculation frequency settings

### Indicators
- `indicator.md` - Indicator development overview
- `addplot.md` - Adding plots to indicators
- `addline.md` - Adding reference lines
- `developing_indicators.md` - Tutorial index

### Strategies  
- `strategy.md` - Strategy development overview
- `enterlong.md`, `entershort.md` - Entry methods
- `exitlong.md`, `exitshort.md` - Exit methods
- `setstoploss.md`, `setprofittarget.md` - Risk management
- `developing_strategies.md` - Tutorial index

### Order Management
- `order_methods.md` - Order method overview
- `managed_approach.md` - Managed order handling
- `unmanaged_approach.md` - Advanced order handling

### Drawing & Charts
- `drawing.md` - Drawing tools overview
- `draw_objects.md` - Draw method reference
- `charts.md` - Chart access and control

### Built-in Indicators
- `moving_average_simple_sma.md`, `moving_average_exponential_ema.md`
- `relative_strength_index_rsi.md`, `stochastics.md`
- `bollinger_bands.md`, `average_true_range_atr.md`
- And 100+ more system indicators

## How to Use

When writing or reviewing NinjaScript code:
1. **Start with best-practices/** - Read `best-practices/index.md` first for coding standards
2. **Check docs/** for API reference - Method signatures, parameters, and examples
3. **Reference education/** for conceptual understanding and tutorials

### Recommended Workflow for Building Indicators
1. Read `docs/indicator.md` for the base class overview
2. Read `docs/onstatechange.md` and `docs/onbarupdate.md` for lifecycle
3. Check `docs/addplot.md` and `docs/addline.md` for visual output
4. Review `best-practices/index.md` for state management patterns

### Recommended Workflow for Building Strategies
1. Read `docs/strategy.md` for the base class overview
2. Read `docs/managed_approach.md` vs `docs/unmanaged_approach.md`
3. Check entry methods: `docs/enterlong.md`, `docs/entershort.md`
4. Check exit methods: `docs/exitlong.md`, `docs/exitshort.md`
5. Review risk management: `docs/setstoploss.md`, `docs/setprofittarget.md`

_Generated on 2026-04-28_
