# Changelog

## v1.4.0 - Sync and Maintenance
- **File Sync**: Updated repository with missing local development files.
- **Version Bump**: Incremented version to 1.4.0.

## v1.3.0 - Ascension Compatibility Update

### 🛠️ Critical Fixes
- **Initialization Overhaul**: Removed duplicate `Initialize` function that was causing "OmniBar has already been added" errors on startup.
- **Chat Channel Guard**: Fixed "Unknown addon chat type" error by preventing `SendCommMessage` from firing when no valid distribution channel (Party/Raid/Guild) is available.
- **ElvUI Enhanced Compatibility**: Patched `AddonsCompatibility.lua` in ElvUI_Enhanced (via documentation) to handle OmniBar's bar-based structure, preventing startup crashes.
- **Syntax Fixes**: Resolved Lua syntax error (`'end' expected`) in `OmniBar.lua`.
- **Scope Fixes**: Fixed `SPELL_ID_BY_NAME` nil value errors by correcting variable scope and removing shadowed declarations.

### 🌟 New Features
- **Ascension Spell Support**: Implemented a name-based fallback system for spell detection. This allows OmniBar to track Ascension custom spells even if their IDs don't match standard WotLK data, backported from `TurboDebuffs`.
- **Shimmed APIs**: added shims for missing Retail APIs (`C_PvP`, `C_Timer`, `SetClipsChildren`, etc.) to ensure smooth operation on the 3.3.5a client.

### 💅 UX Improvements
- **Tooltip Cleanup**: Removed misleading "Hold SHIFT for more information" text from OmniBar option tooltips, as this server-side text is non-functional in the addon settings.
