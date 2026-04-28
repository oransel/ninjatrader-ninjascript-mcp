# NinjaTrader NinjaScript Knowledge Base

A comprehensive, LLM-ready knowledge base of the [NinjaTrader Desktop SDK documentation](https://developer.ninjatrader.com/docs/desktop) for building indicators and strategies with AI coding assistants.

## What's Included

| Folder | Contents | Files |
|--------|----------|-------|
| `docs/` | Complete API reference | 1066 |
| `education/` | Learning resources & tutorials | 1 |
| `best-practices/` | NinjaScript coding guidelines | 1 |

**Total: 1068 documentation pages**

## Quick Start

### Option 1: MCP Server (Recommended)

Use the MCP server for dynamic, on-demand access to the documentation:

```json
{
  "mcpServers": {
    "ninjatrader": {
      "command": "npx",
      "args": ["-y", "ninjatrader-ninjascript-mcp"]
    }
  }
}
```

Add this to your MCP config file:

| Tool | Platform | Config Path |
|------|----------|-------------|
| Kiro | macOS/Linux | `~/.kiro/settings/mcp.json` |
| Kiro | Windows | `%USERPROFILE%\.kiro\settings\mcp.json` |
| Claude Desktop | macOS | `~/Library/Application Support/Claude/claude_desktop_config.json` |
| Claude Desktop | Windows | `%APPDATA%\Claude\claude_desktop_config.json` |
| Claude Desktop | Linux | `~/.config/Claude/claude_desktop_config.json` |

The MCP server provides tools to search docs, get specific pages, and follow recommended workflows.

### Option 2: Static Files

#### Claude Code / Kiro

Copy `CLAUDE.md` to your project root, or add this to your existing `CLAUDE.md`:

```markdown
## NinjaTrader Docs
Full SDK reference is in ./path/to/this/repo/. When writing NinjaScript,
consult the relevant .md files for accurate API signatures and examples.
```

#### OpenCode

Copy `RULES.md` to your `.opencode/` folder:

```bash
cp RULES.md /path/to/your/project/.opencode/rules.md
```

#### Other AI Tools

Point your AI assistant to this directory. The `index.json` file contains a machine-readable index of all pages.

## Example Files for Common Tasks

### Building Indicators
- `docs/indicator.md` - Base class overview
- `docs/onstatechange.md` - Lifecycle management
- `docs/onbarupdate.md` - Calculation logic
- `docs/addplot.md` - Adding visual plots
- `best-practices/index.md` - Coding standards

### Building Strategies
- `docs/strategy.md` - Base class overview
- `docs/managed_approach.md` - Order management
- `docs/enterlong.md`, `docs/entershort.md` - Entry methods
- `docs/setstoploss.md`, `docs/setprofittarget.md` - Risk management

## File Structure

All documentation files in `docs/` use a flat structure with filenames derived from the original URL:
- `enterlong.md` ← from `https://developer.ninjatrader.com/docs/desktop/enterlong`
- `moving_average_simple_sma.md` ← from `https://developer.ninjatrader.com/docs/desktop/moving_average_simple_sma`
- `onstatechange.md` ← from `https://developer.ninjatrader.com/docs/desktop/onstatechange`

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Support

If this project helped you, consider supporting its development:

- [PayPal](https://paypal.me/AIMustafa)
- BTC: `18gT1wmq3RMoLBm2ZFv4PhiYbU5CMAQC6P`

## Links

- [NinjaTrader Official Website](https://ninjatrader.com)
- [NinjaTrader Developer Documentation](https://developer.ninjatrader.com/docs/desktop)
- [GitHub Repository](https://github.com/oransel/ninjatrader-ninjascript-kb)
- [MCP Server on npm](https://www.npmjs.com/package/ninjatrader-ninjascript-mcp)

## License

Copyright (c) 2026 Mustafa Oransel

This library is free software; you can redistribute it and/or modify it under the terms of the GNU Lesser General Public License as published by the Free Software Foundation; either version 3 of the License, or (at your option) any later version.

This library is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU Lesser General Public License for more details.

Note: The documentation content in this repository is sourced from NinjaTrader's official developer documentation. Please refer to NinjaTrader's terms of use regarding the use of their documentation.

---

_Last updated: 2026-04-28_
