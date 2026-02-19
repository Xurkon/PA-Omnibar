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
