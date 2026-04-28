# NinjaTrader Desktop SDK Knowledge Base

Full API reference mirror from https://developer.ninjatrader.com/docs/desktop.

## Structure

```
├── docs/               ← Main API documentation (1066 files)
├── education/          ← Educational resources
└── best-practices/     ← NinjaScript coding guidelines
```

## When to Use

When the user asks about NinjaScript APIs, strategies, indicators, or drawing
tools, read the appropriate file(s) from this directory before answering.

## How to Use

1. **Start with best-practices/** - Read `best-practices/index.md` first for coding standards
2. **Check docs/** for API reference - Method signatures, parameters, and examples
3. **Reference education/** for conceptual understanding and tutorials

### Workflow for Building Indicators
1. Read `docs/indicator.md` for the base class overview
2. Read `docs/onstatechange.md` and `docs/onbarupdate.md` for lifecycle
3. Check `docs/addplot.md` and `docs/addline.md` for visual output
4. Review `best-practices/index.md` for state management patterns

### Workflow for Building Strategies
1. Read `docs/strategy.md` for the base class overview
2. Read `docs/managed_approach.md` vs `docs/unmanaged_approach.md`
3. Check entry methods: `docs/enterlong.md`, `docs/entershort.md`
4. Check exit methods: `docs/exitlong.md`, `docs/exitshort.md`
5. Review risk management: `docs/setstoploss.md`, `docs/setprofittarget.md`

## Key Files Quick Reference

### Core Concepts
- `docs/onstatechange.md` - Lifecycle management
- `docs/onbarupdate.md` - Main calculation method
- `docs/calculate.md` - Calculation frequency settings

### Indicators
- `docs/indicator.md` - Indicator base class
- `docs/addplot.md` - Adding plots
- `docs/addline.md` - Adding reference lines

### Strategies
- `docs/strategy.md` - Strategy base class
- `docs/enterlong.md`, `docs/entershort.md` - Entry methods
- `docs/exitlong.md`, `docs/exitshort.md` - Exit methods
- `docs/setstoploss.md`, `docs/setprofittarget.md` - Risk management
- `docs/managed_approach.md` - Managed order handling
- `docs/unmanaged_approach.md` - Advanced order handling

### Drawing & Charts
- `docs/drawing.md` - Drawing tools overview
- `docs/draw_objects.md` - Draw method reference

## File Naming

All docs are flat in `docs/` — named after URL path:
- `.../docs/desktop/enterlong` → `docs/enterlong.md`
