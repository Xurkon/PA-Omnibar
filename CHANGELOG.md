# Changelog

## v1.5.1 - Options Loading Fix
- **FIXED**: Critical issue where `Options.lua` failed to load in 3.3.5a due to missing `WOW_PROJECT_ID` definitions, causing `/omnibar` slash command to fail.
- **FIXED**: Typo in `Options.lua` variable name.

## v1.5.0 - Combat Log Spec Detection & Bug Fixes

### 🌟 New Features
- **Combat Log Spec Detection**: Implemented advanced spec detection for arena/PvP using combat log event sniffing (adapted from Gladdy addon).
  - Added 130+ spell/buff-to-spec mappings for all classes
  - Detects enemy specs from signature spell casts and buff applications
  - Enables accurate spec-specific cooldown adjustments in arena without inspection
  - Validates detected specs against player class to prevent false positives

### 🛠️ Bug Fixes
- **Guild Chat Error**: Fixed "Unknown addon chat type" error when not in a guild on certain realms (e.g., Bronzebeard - Warcraft Reborn).
  - Added validation to prevent sending addon messages to GUILD channel when not guild member

### 📝 Technical Details
- New `SPEC_SPELLS` table: Maps offensive spells to specs (e.g., Penance → Discipline)
- New `SPEC_BUFFS` table: Maps buffs/debuffs to specs (e.g., Shadowform → Shadow)
- New `TrySetSpec()` function: Validates detected specs using `GetPlayerInfoByGUID()`
- Enhanced `COMBAT_LOG_EVENT_UNFILTERED` handler for spec detection on 3.3.5a clients


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
