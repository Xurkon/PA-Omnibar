<div align="center">

# PA-Omnibar

![Version](https://img.shields.io/badge/version-v1.3.0-blue.svg?style=for-the-badge)
![Downloads](https://img.shields.io/github/downloads/Xurkon/PA-Omnibar/total?style=for-the-badge&color=e67e22)
[![Documentation](https://img.shields.io/badge/Documentation-View%20Docs-58a6ff?style=for-the-badge)](docs/index.html)
[![Patreon](https://img.shields.io/badge/Patreon-F96854?style=for-the-badge&logo=patreon&logoColor=white)](https://www.patreon.com/Xurkon)
[![PayPal](https://img.shields.io/badge/PayPal-00457C?style=for-the-badge&logo=paypal&logoColor=white)](https://www.paypal.me/Xurkon)
![License](https://img.shields.io/github/license/Xurkon/PA-Omnibar?style=for-the-badge&color=2980b9)
![Platform](https://img.shields.io/badge/PLATFORM-WotLK%203.3.5a-blue?style=for-the-badge&logo=windows&logoColor=white)

<br/>
**Advanced Enemy Cooldown Tracker for Project Ascension**

[⬇ **Download Latest**](https://github.com/Xurkon/PA-Omnibar/releases/latest) &nbsp;&nbsp;•&nbsp;&nbsp; [📂 **View Source**](https://github.com/Xurkon/PA-Omnibar) &nbsp;&nbsp;•&nbsp;&nbsp; [📖 **Read Documentation**](docs/index.html)

</div>

---

## ✨ Features

### 🌍 Ascension Support
- **Custom Spell Detection**: Fully compatible with Project Ascension's custom spell IDs.
- **Name-Based Lookup**: Intellgiently falls back to spell names when IDs change (essential for custom servers).
- **ElvUI Compatibility**: Patched to work seamlessly with ElvUI Enhanced on 3.3.5a.

### ⚔️ PvP Dominance
- **Track Enemy Cooldowns**: Monitor interrupts, defensive, and offensive abilities in real-time.
- **Arena & Battleground Ready**: Automatically adjusts visibility based on zone and rated status.
- **Multiple Bars**: Organize cooldowns into separate bars (e.g., Interrupts, Defensives).

### 🎨 Visual Customization
- **Glow Animations**: Icons glow when an ability is used.
- **Cooldown Numbers**: Integrates with OmniCC or Blizzard's cooldown text.
- **Masque Support**: Skin icons to match your UI.
- **Transparency Control**: Adjust opacity for used and unused icons or swipe animations.

## 📥 Installation

1. Download the addon.
2. Extract the `OmniBar` folder to your `Interface\AddOns` directory.
3. Reload your UI (`/reload`).

## 🔧 Usage

1. **Open Settings**: Type `/ob` or `/omnibar` in chat.
2. **Unlock Bars**: Uncheck "Lock" to move bars around.
3. **Select Spells**: Go to the "Spells" tab to choose which cooldowns to track.
4. **Create Bars**: Create new bars for different categories of spells.

## 📜 Changelog

See [CHANGELOG.md](CHANGELOG.md) for full version history.

### v1.3.0 - Ascension Compatibility Patch
- **FIXED**: Critical initialization errors "OmniBar has already been added".
- **FIXED**: "Unknown addon chat type" error when playing solo.
- **ADDED**: Name-based spell detection for Ascension custom spells.
- **FIXED**: ElvUI Enhanced compatibility (nil table error).
- **FIXED**: Removed misleading "Hold SHIFT" text from tooltips.

## 👥 Credits

- **Jordon** - Original Author
- **Xurkon** - Ascension Compatibility Fixes
- **Project Ascension** - For the unique classless experience

## 📄 License

MIT License
