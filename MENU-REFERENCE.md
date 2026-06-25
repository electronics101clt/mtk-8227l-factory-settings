# Factory Settings Menu Reference

Complete listing of all menu entries in Parameter Settings ver2.7_20181022.

---

## Mounting Vehicle Settings (100 Series)

### 101 - Backcar Delay Time
**Status**: ✅ Documented
**Purpose**: Controls delay before backup camera view activates when shifting into reverse gear
**Interface**: Slider control (adjustable in seconds)
**Range**: 0.5s - several seconds
**Default**: 0.5s
**Screenshot**: [101-backcar-delay-time.png](screenshots/101-backcar-delay-time.png)
**Notes**: Prevents instant camera switching if briefly engaging reverse gear. Allows fine-tuning activation timing.

### 102 - Mute Settings
**Status**: Undocumented
**Purpose**: Audio muting configuration
**Notes**:

### 103 - Protocol Settings
**Status**: Undocumented
**Purpose**: Communication protocol configuration (CAN bus, steering wheel controls)
**Notes**:

### 104 - Reboot
**Status**: Documented
**Purpose**: System reboot
**Notes**: Restarts the Android system

### 105 - Camera And Protocol Parameter Settings
**Status**: Undocumented
**Purpose**: Backup/front camera and protocol parameter configuration
**Notes**:

### 106 - Help and Feedback
**Status**: Undocumented
**Purpose**: Support/feedback interface
**Notes**:

### 107 - Protocol Debugging
**Status**: Undocumented
**Purpose**: Debug communication protocols
**Notes**: Likely for CAN bus diagnostics

### 108 - Power Amplifier Settings
**Status**: Undocumented
**Purpose**: Audio amplifier configuration
**Notes**: May control external amp settings

---

## Factory Settings (300 Series)

### 301 - Color Settings
**Status**: Partially Documented
**Purpose**: Display color calibration
**Related**: PIN code 1616 provides access to brightness, contrast, hue, saturation controls
**Notes**: Factory display calibration tool

### 302 - Production Management
**Status**: Undocumented
**Purpose**: Manufacturing and quality control settings
**Notes**: Likely used during production line testing

### 303 - Touch Settings
**Status**: Partially Documented
**Purpose**: Touchscreen calibration
**Related**: Touch calibration tools mentioned in XDA forums
**Notes**: Used to calibrate touch panel accuracy

### 304 - Export The Config
**Status**: Partially Documented
**Purpose**: Backup/export settings
**Related**: PIN code 5555 exports advanced settings to SD/USB
**Notes**: Configuration backup functionality

### 305 - Direction Control Settings
**Status**: Undocumented
**Purpose**: UNKNOWN - Possibly screen orientation, navigation bar position, or steering wheel control direction
**Notes**: **PRIMARY RESEARCH TARGET** - This setting may control navigation bar placement

### 306 - IR Code Output Settings
**Status**: Undocumented
**Purpose**: Infrared remote control configuration
**Notes**: Likely for steering wheel control IR codes

### 307 - Encoder Settings
**Status**: Partially Documented
**Purpose**: Volume knob/rotary encoder configuration
**Related**: Hardware encoder mapping and calibration
**Notes**: Configures quadrature encoder inputs for volume knob

### 308 - Physical Buttons Study
**Status**: Documented
**Purpose**: Physical button learning/mapping
**Related**: Mentioned in XDA forums as accessible via 8888 code
**Notes**: Learn and map physical buttons to functions

### 309 - Tire Pressure Settings
**Status**: Undocumented
**Purpose**: TPMS (Tire Pressure Monitoring System) integration
**Notes**: Configuration for tire pressure sensors

### 310 - Lock Screen Mode Settings
**Status**: Undocumented
**Purpose**: Lock screen behavior configuration
**Notes**: May control password lock screen

### 311 - Key Light Settings
**Status**: Undocumented
**Purpose**: Button backlight/illumination settings
**Notes**: Controls physical button LED illumination

---

## Engineering Settings (700 Series)

### 701 - USB Settings
**Status**: Undocumented
**Purpose**: USB port configuration
**Notes**: May control USB modes (host/device/OTG)

### 702 - Clear Test File
**Status**: Undocumented
**Purpose**: Remove test/diagnostic files
**Notes**: Cleanup tool for manufacturing test data

### 703 - Debug Touch
**Status**: Undocumented
**Purpose**: Touchscreen debugging interface
**Notes**: Visual touch input debugging

### 704 - App Settings
**Status**: Undocumented
**Purpose**: Application-level configuration
**Notes**: May access hidden app settings

### 705 - Touch Test
**Status**: Undocumented
**Purpose**: Touchscreen testing utility
**Notes**: Interactive touch calibration test

### 706 - Bluetooth Connect Pair Set
**Status**: Undocumented
**Purpose**: Bluetooth pairing configuration
**Notes**: Advanced BT pairing settings

### 707 - MCU Info Test
**Status**: Undocumented
**Purpose**: Microcontroller information and testing
**Notes**: Displays MCU firmware version and diagnostics

### 708 - Engineering Test Debugging
**Status**: Undocumented
**Purpose**: General engineering diagnostics
**Notes**: Comprehensive system testing interface

---

## Legend

**Status Categories:**
- **Undocumented**: No online documentation found
- **Partially Documented**: Some information available, needs verification
- **Documented**: Well-documented with confirmed functionality

---

## Research Priority

High priority items for further investigation:
1. **305 - Direction Control Settings** (navigation bar positioning)
2. **301 - Color Settings** (display calibration details)
3. **307 - Encoder Settings** (volume knob configuration)
4. **103 - Protocol Settings** (CAN bus configuration)
5. **707 - MCU Info Test** (firmware information)
