# Research Notes

Documentation of research findings and search results for MTK 8227L factory settings.

## Date: 2026-06-25

### Search Summary

Conducted extensive searches on XDA Forums and general web for information about Parameter Settings ver2.7_20181022 and the numbered menu system.

### Key Findings

#### Firmware Version Information

- **"ver2.7_20181022"**: Appears in MTK 8227L_Demo RDS Radio APK thread on XDA
  - Build date format suggests: October 22, 2018
  - Version 2.7 of the parameter settings interface
  - Source: [MTK 8227l_Demo RDS Radio APK | XDA Forums](https://xdaforums.com/t/mtk-8227l_demo-rds-radio-apk.4080677/)

#### Access Codes (Confirmed)

Well-documented codes for 8227L units:
- **8888**: Factory settings access (most common)
- **5678**: Custom boot logo window
- **1414**: Reboot system and save settings
- **1111**: Memory status real-time
- **5555**: Export advanced settings to SD/USB
- **1616**: Brightness, contrast, hue, saturation, tone controls
- **2134**: TsMainUI8 window (all folders/apps selectable)

Sources:
- [How to access Engineering Mode for AC8227L | XDA Forums](https://xdaforums.com/t/how-to-access-engineering-mode-for-ac8227l.4592425/)
- [ALPS FF5000 & other headunits (8227L) pin codes for factory menus | XDA Forums](https://xdaforums.com/t/alps-ff5000-other-headunits-8227l-pin-codes-for-factory-menus.4269431/)

#### Numbering System

**No explicit documentation found** for the 100/300/700 numbering scheme.

**Working hypothesis:**
- **100 series**: Vehicle integration settings (mounting-specific)
- **300 series**: Factory production settings (hardware calibration)
- **700 series**: Engineering/diagnostic tools (testing and debug)

The numbering appears to be:
- Manufacturer-specific (not a MediaTek standard)
- Used for factory worker reference
- Language-agnostic (numbers work globally)
- Service manual indexing

#### Menu Entry Research

##### 301 - Color Settings
- Related to display calibration
- PIN code 1616 provides access to brightness/contrast/hue/saturation/tone
- File mentioned: `/storage/emulated/0/calibration.ini`
- **No specific documentation** about menu 301 found

##### 305 - Direction Control Settings
- **Zero documentation found**
- Hypothesis: Could control:
  - Screen orientation
  - Navigation bar position (top/bottom)
  - Steering wheel control direction mapping
  - Display rotation settings

##### 307 - Encoder Settings
- Related to rotary volume knob configuration
- Hardware encoder types use different resistor values
- Quadrature encoder input configuration
- "Knob mode" setting mentioned in factory settings
- Sources:
  - [Android Head Unit Gets Volume Knob Upgrade | Hackaday](https://hackaday.com/2025/01/17/android-head-unit-gets-volume-knob-upgrade/)
  - [Volume Control for a Android Head Unit – Westaby Home](https://www.westaby.net/2017/10/volume-control-for-a-android-head-unit/)

##### 308 - Physical Buttons Study
- **Confirmed**: Button learning/mapping functionality
- Accessible via 8888 password
- Used to teach the unit physical button functions

### Gaps in Documentation

The following menu items have **zero online documentation**:
- 101: Backcar Delay Time
- 102: Mute Settings
- 103: Protocol Settings
- 105: Camera And Protocol Parameter Settings
- 106: Help and Feedback
- 107: Protocol Debugging
- 108: Power Amplifier Settings
- 302: Production Management
- 306: IR Code Output Settings
- 309: Tire Pressure Settings
- 310: Lock Screen Mode Settings
- 311: Key Light Settings
- 701: USB Settings
- 702: Clear Test File
- 703: Debug Touch
- 704: App Settings
- 705: Touch Test
- 706: Bluetooth Connect Pair Set
- 707: MCU Info Test
- 708: Engineering Test Debugging

### XDA Forum Threads Reviewed

1. [8227L android unit 8.1 chinese](https://xdaforums.com/t/8227l-android-unit-8-1-chinese.3905535/) - Main discussion thread
2. [How to access Engineering Mode for AC8227L](https://xdaforums.com/t/how-to-access-engineering-mode-for-ac8227l.4592425/) - Access codes
3. [ALPS FF5000 & other headunits (8227L) pin codes](https://xdaforums.com/t/alps-ff5000-other-headunits-8227l-pin-codes-for-factory-menus.4269431/) - PIN codes
4. [Collection of 8227l firmware](https://forum.xda-developers.com/android-auto/android-head-units/collection-8227l-firmware-android-vers6-t4003935) - Firmware collection
5. [Factory Settings Menu](https://xdaforums.com/t/factory-settings-menu.3250647/) - General factory settings

### Next Steps

1. **Test menu entries directly** - Access each menu to document actual functionality
2. **Explore 305** - Test Direction Control Settings to determine if it controls nav bar position
3. **Community outreach** - Post on XDA Forums requesting info about specific menu numbers
4. **APK decompilation** - Examine factory settings APK to find menu definitions
5. **MCU firmware analysis** - Menu 707 may reveal MCU version info

### Device Information

Testing performed on:
- **Device**: Android car head unit
- **Chipset**: MTK 8227L
- **Firmware**: Parameter Settings ver2.7_20181022
- **Connection**: ADB over USB
- **Device ID**: M7YHEIB69SSSSSA6

### Original Issue

User reported navigation bar moved from top (integrated with status bar) to bottom of screen. Attempting to identify which factory setting controls this behavior.

**Suspected menu**: 305 - Direction Control Settings

---

## Utility Screens Found During Exploration

### Protocol Box Upgrade Utility

**Discovered**: 2026-06-25
**Access**: Via menu 105 or 107 (CANBUS/Protocol settings submenu)

**Interface**:
- Protocol box upgrade screen
- "Selection of agreement company" dropdown
- "upgrade" button

**Purpose**: Firmware upgrade utility for CANBUS protocol box
- Updates CANBUS adapter firmware
- Manufacturer-specific protocol updates
- "Agreement company" = CANBUS protocol vendor selection

**XDA Research**:
- CANBUS boxes use manufacturer-specific protocols
- Firmware updates available via factory menu
- Chinese FTP server (xygala software) contains protocol firmware files
- Factory settings includes CANBUS configuration options
- Protocol Settings (menu 103) related to this upgrade utility

**Sources**:
- [Collection of 8227l firmware (android vers:6-9) | XDA Forums](https://xdaforums.com/t/collection-of-8227l-firmware-android-vers-6-9.4003935/)
- [8227L YT9216BJ Head Unit | XDA Forums](https://xdaforums.com/t/8227l-yt9216bj-head-unit.4139307/)

**Notes**: Not a numbered main menu entry. Utility screen accessible from CANBUS/protocol configuration menus. Critical for updating vehicle-specific CANBUS protocol definitions.
