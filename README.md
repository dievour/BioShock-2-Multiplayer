![BioShock 2 Multiplayer](Images/BioShockStartupBigSisterDuo.png)
# BioShock 2 Multiplayer — UserFixes

A plugin for *BioShock 2 Multiplayer* that applies persistent user preferences on launch via a simple INI configuration file.

---

## 🌊 Overview

**UserFixes** is designed to be used alongside [BioShock 2 Multiplayer Plugins](https://github.com/SnowTempest/Bioshock-2-Multiplayer-Plugins) by SnowTempest. It is distributed as a plugin DLL intended to be loaded through the **BioPlugins** plugin loader.

No overlays, no menus — configure your preferences once, and they apply automatically every session.

---

## 🌊 Features

- **FOV Configuration** — Set your desired field of view for gameplay and weapons
- **Mouse Settings** — Disable mouse smoothing and acceleration for raw input
- **Crouch Height Fix** — Allows players to enter smaller spaces, such as vents on certain maps that were previously inaccessible due to an incorrect default crouch height value

---

## 🌊 Requirements

- BioShock 2 Multiplayer (Steam)
- [BioShock 2 Multiplayer Plugins](https://github.com/SnowTempest/Bioshock-2-Multiplayer-Plugins) by SnowTempest — required to load UserFixes as a plugin

---

## 🌊 Installation

1. Download and set up [BioShock 2 Multiplayer Plugins](https://github.com/SnowTempest/Bioshock-2-Multiplayer-Plugins) first
2. Download the latest release of UserFixes from the [Releases](https://github.com/dievour/BioShock-2-Multiplayer/releases) page
3. Place `UserFixes.dll` inside the `BioPlugins` folder:

```
\SteamLibrary\steamapps\common\BioShock 2\MP\Builds\Binaries\
├── BioShock2.exe
├── dxgi.dll
└── BioPlugins\
    ├── MicFix.dll
    └── UserFixes.dll   ← place here
```

4. Launch the game — `UserPreferences.ini` will be created automatically on first run at:
```
%APPDATA%\Bioshock2Steam\UserPreferences.ini
```
5. Close the game, edit the INI with your preferred settings, and relaunch

---

## 🌊 Configuration

The INI file is located at:
```
%APPDATA%\Bioshock2Steam\UserPreferences.ini
```

```ini
; Made by dievour
; BioShock 2 User Preferences Configuration
; Edit the values below and relaunch the game to apply.
; Modifying these values during a match will not update your configuration.

[FOV]
; The field of view used during normal gameplay
DesiredFOV=90.0

; The base field of view the game defaults to (should match DesiredFOV in most cases)
DefaultFOV=90.0

; The field of view applied to the weapon/hands in first person
DefaultForeGroundFOV=70.0

[Mouse]
; Controls mouse smoothing. 0 = disabled (raw input), 1 = enabled
MouseSmoothingMode=0

; Controls mouse acceleration. 0.0 = disabled (1:1 movement), higher values = more acceleration
MouseAccel=0.0

[Player]
; Enable crouch height fix to allow entering smaller spaces like vents for certain maps.
; true = enabled, false = disabled
CrouchHeightFix=false
```

---

## 🌊 Notes

- Settings are applied automatically on each game and level load
- The crouch height fix reapplies automatically after death
- If you have an existing `UserPreferences.ini` from a previous version, any missing settings will be added automatically — you do not need to delete your existing file
- Modifying the INI while the game is running will not take effect until the next load

---

## 🌊 Plugin Safety

Please refer to the [Plugin Safety](https://github.com/SnowTempest/Bioshock-2-Multiplayer-Plugins#%EF%B8%8F-plugin-safety) section in the BioShock 2 Multiplayer Plugins repository for general guidance on plugin safety.

---

## 🌊 False Positive Antivirus Detections

As with all plugin DLLs, some antivirus software may flag this file as suspicious. This is a known false positive caused by the nature of DLL injection and runtime memory modification. If you are uncomfortable, do not install it.

---

## 🌊 Copyright

UserFixes is an unofficial, non-commercial community plugin for BioShock 2 Multiplayer. All original game content, including assets, characters, story, and company names, are the property of 2K Games.

This plugin is intended for players who already own a legitimate copy of BioShock 2. It is not an official download, patch, or product from 2K Games or Digital Extremes.
