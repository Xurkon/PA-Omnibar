# OmniBar (Project Ascension Edition)

OmniBar is a lightweight addon that tracks enemy cooldowns on their nameplates and in a standalone bar. It is essential for PvP, allowing you to see when opponents have used critical interrupts, defensive cooldowns, and crowd control abilities.

> [!IMPORTANT]
> This is a customized version for **Project Ascension** (3.3.5a client). 
> It has been refactored to use **native API calls** instead of external backport libraries or polyfills, ensuring maximum performance and compatibility with Ascension's custom class system.

## Features

- **Enemy Cooldown Tracking**: Automatically detects and displays cooldowns used by enemies.
- **Project Ascension Support**: Fully compatible with Ascension's custom classes and abilities.
- **Native Performance**: No dependencies on `!!!ClassicAPI` or other backport libraries. Uses efficient, native 3.3.5a code.
- **Customizable**:
  - Unlock and move the bar anywhere.
  - Test mode to configure the look and feel.
  - "Show Unused" icons option to see what cooldowns opponents *could* use.
- **Lightweight**: Optimized to have minimal impact on game performance.

## Help Wanted

We need players to help test this in various combat scenarios:
- **Arenas**: Verify enemy cooldowns track correctly in all brackets.
- **Battlegrounds**: Ensure performance remains high in large-scale PvP.
- **World PvP**: Confirm tracking works in the open world.

**Please report any Lua errors or issues where cooldowns do not appear correctly on my GitHub Issues page.**

## Documentation

For full usage instructions and configuration details, please see the [Documentation](docs/index.html).
