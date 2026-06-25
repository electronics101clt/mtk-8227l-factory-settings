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
**Notes**: Prevents instant camera switching if briefly engaging reverse gear. Allows fine-tuning activation timing.

### 102 - Mute Settings
**Status**: ✅ Documented
**Purpose**: Configure audio muting behavior and voltage detection threshold
**Interface**: Voltage slider + 3 checkboxes
**Options**:
- **Voltage value**: ACC/mute wire voltage detection threshold (slider: 7V default)
- **Hardware mute switch**: Enable physical mute wire input
- **Key mute switch**: Enable mute button (steering wheel/panel)
- **Mute switch during startup**: Mute audio during system boot
**XDA References**: ACC voltage behavior discussed in power management threads
**Notes**: Voltage threshold determines when ACC signal is recognized. All checkboxes enabled by default.

### 103 - Protocol Settings
**Status**: ✅ Documented
**Purpose**: CAN bus protocol configuration for vehicle integration
**Interface**: CAN Set screen (V9.10.0.disconnect)
**Options**:
- **Vehicle manufacturer selection**: Raise, XINPU, Hiworld, XBS, BNR, Daojun
- **Car model selection**: Hyundai KIA, GM, Peugeot, Jeep, Mazda, GAC, BAIC
- **CAN ID display**: Shows current CAN identifier (e.g., 1006002)
- **Network button**: Protocol configuration options
**XDA References**:
- Raise CAN bus adapters translate CAN to serial TTL (19200 baud, 8N1)
- Settings include NORMAL/SWAP options for CAN TYPE/CANBUS
- Required for steering wheel control configuration
- Warning: Some users report menu kicks them out after access
**Notes**: Configures vehicle-specific CAN bus protocol for steering wheel controls, vehicle data integration. Critical for proper vehicle interface communication.

### 104 - Reboot
**Status**: Documented
**Purpose**: System reboot
**Notes**: Restarts the Android system

### 105 - Camera And Protocol Parameter Settings
**Status**: ✅ Documented
**Purpose**: Comprehensive backup/reverse camera, 360 camera, and vehicle integration configuration
**Interface**: Reversing Settings submenu with 26+ scrollable options
**Options**:
- **Reverse track settings**: Parking trajectory line configuration
- **Reverse radar settings**: Parking sensor/radar overlay configuration
- **Reverse image Settings**: Camera image adjustments (flip, mirror, brightness)
- **Reverse color Settings**: Color calibration for backup camera
- **Reverse trajectory direction settings**: Trajectory line angle/direction calibration
- **Door information settings**: Door status integration with camera display
- **Agreement party accused of settings**: (Translation unclear - likely protocol agreement settings)
- **360 Camera**: 360-degree camera system configuration
- **Audio port**: Audio routing for reverse camera (speakers selection)
- **Reverse lay the auxiliary line**: Auxiliary/trajectory line overlay enable/disable
- **Pop air settings**: (Translation unclear - possibly parking sensor alerts)
- **Reversing camera angle switch settings**: Camera view angle adjustment
- **Parking radar settings**: Parking sensor configuration and thresholds
- **Right view switch Settings**: Right-side camera view configuration
- **Reverse video resolution settings**: Camera resolution selection
- **Software astern**: Software-based reverse detection (vs hardware trigger)
- **SYNC switch**: Synchronization settings for multi-camera systems
- **UI settings**: User interface configuration for camera views
- **Outside input and right view resolution settings**: External camera input and resolution
- **Front view switching time**: Delay before switching to front camera view
- **Agreement model alarm box**: Alarm/notification settings for camera events
- **Air conditioner floating key switch**: AC control overlay display (requires restart)
- **Temperature unit**: Celsius/Fahrenheit selection for temperature display
- **Bagu protocol box controls the original car function switch**: Factory vehicle function integration via CANBUS
- **Door state switch**: Door open/close status monitoring and display
**XDA References**:
- Factory settings access via password 8888
- TCON/video settings must be configured for third-party video
- Common issues: "NO SIGNAL" errors, camera loops
- Parking radar sensors may not produce beep sounds (configuration issue)
- Assistant lines sometimes built into camera (cannot disable in software)
- AC display and vehicle integration via CANBUS box if equipped
- Auto speed volume and dimming connected to CANBUS device
**Notes**: Comprehensive camera system configuration including trajectory overlays, radar integration, multi-camera setups, AND vehicle integration features (AC, temperature, door status). Requires CANBUS adapter for vehicle data integration. Menu contains 26+ scrollable options.

### 106 - Help and Feedback
**Status**: Undocumented
**Purpose**: Support/feedback interface
**Notes**:

### 107 - Protocol Debugging
**Status**: ✅ Documented
**Purpose**: Real-time CANBUS protocol debugging and log monitoring
**Interface**: Program log display with control buttons
**Options**:
- **protocol...**: Protocol selection/configuration button
- **print data**: Output log data to screen/file
- **time cha...**: Time-related controls (timestamp display)
- **clear log**: Clear the debug log display
**Display**: Black log area showing real-time protocol communications
**XDA References**:
- CANBUS debugger shows when steering wheel controls are pressed
- Detects if RAISE canbus box decoder is connected
- Used for diagnosing protocol communication issues
- Engineering Mode accessible via Factory Settings → USB Info → USB
**Notes**: Critical tool for debugging CANBUS communication, steering wheel controls, and vehicle integration. Shows real-time protocol data stream for troubleshooting.

### 108 - Power Amplifier Settings
**Status**: ✅ Documented
**Purpose**: Power amplifier gain/output level configuration
**Interface**: Percentage slider with control buttons
**Options**:
- **Percent slider**: Amplifier power level (0-100%)
- **Minus/Plus buttons**: Adjust amplifier power
- **OK button**: Save settings
- **default button**: Reset to factory default level
**Range**: 0-100% (currently set to 100)
**XDA References**:
- Access via factory settings (password 8888)
- Recommended to set around 50% to avoid distortion
- Can activate DSP effects (set to value "1")
- Can enable AMP (set to value "1")
- VOLUME menu section in factory settings controls all audio levels
- Amplifier chip varies by manufacturer
**Notes**: Controls power amplifier output gain. Setting too high causes distortion. Recommended around 50%. Used with external amplifiers or to boost internal amp output. DSP and AMP activation available in related settings.

---

## Factory Settings (300 Series)

### 301 - Color Settings
**Status**: ✅ Documented
**Purpose**: Adjust display screen properties (brightness, contrast, color, saturation)
**Interface**: Settings screen with Asian woman reference image
**Features**:
- Asian woman backdrop as visual reference while adjusting screen
- Display text: "Close the car small light" = turn off dome light (interior cabin light) so screen can be seen clearly
- Multiple "Time" labels (display timing controls)
- Screen adjustment controls for display properties
**Related**: PIN code 1616 provides access to brightness, contrast, hue, saturation, tone controls
**File**: Related to `/storage/emulated/0/calibration.ini`
**XDA References**:
- PIN 1616 for brightness/contrast/hue/saturation/tone controls
- calibration.ini file stores display settings
- "Small light" = dome light (interior cabin light)
- Dome light interferes with viewing screen adjustments
**Notes**: Factory display adjustment tool. Asian woman image provides visual reference for adjusting screen properties. Users must turn off dome light (interior cabin light) so they can see the screen clearly while making adjustments.

### 302 - Production Management
**Status**: ✅ Documented
**Purpose**: Manufacturer-only production line and quality control access
**Interface**: Login screen with account and password fields
**Features**:
- Account input field
- Password input field
- LOGIN button
- Authentication required for access
**XDA References**:
- No public documentation of production account credentials
- Code 12 shows production ID (not account login)
- Engineering mode password: 26959910 (for debugging, not production management)
- Common factory password 8888 (for general factory settings, not this menu)
- This menu appears to be manufacturer/factory-only access
**Notes**: Restricted access menu for production line workers and quality control personnel. Requires manufacturer-specific account credentials not publicly available. Used during manufacturing for production testing and quality assurance. Not accessible to end users without factory login credentials.

### 303 - Touch Settings
**Status**: ✅ Documented
**Purpose**: Touchscreen calibration and touch button mapping
**Interface**: Grid layout with touch test areas and calibration controls
**Grid Layout**:
- **Row 1**: power, home, back, voladd (volume up)
- **Row 2**: voldec (volume down), nokey, nokey, nokey
- **Row 3**: nokey, nokey, start, clear
- **Row 4**: Touch screen resolution, config, key position, The X axis Y axis swap
**Controls**:
- **start**: Begin touch calibration process
- **clear**: Reset/clear calibration data
- **config**: Configure touch button mappings
- **key position**: Set touch button positions
- **Touch screen resolution**: Set correct panel resolution
- **The X axis Y axis swap**: Fix inverted/mirrored touch coordinates
- **nokey**: No key assigned or no touch detected in area
**XDA References**:
- **5-finger calibration**: Put 5 fingers on screen to trigger quick calibration menu (touch 4 spots, select OK)
- **Physical Buttons Study process**: Click start, then touch each button when prompted (home, power, voladd, voldec), shows X/Y coordinates, click OK
- **X/Y axis swap**: Fix for inverted/mirrored touchscreen in items.ini firmware file
- **Calibration file**: `/storage/emulated/0/calibration.ini` stores calibration data
- **GtpAdbTool**: Advanced Goodix touch panel configuration tool (186-byte config file)
- **Common issues**: Left side touch (X0-X200) accuracy problems, touch offset increases moving left/down
- **items.ini**: Firmware file contains touchpanel X/Y axis config (1 or 0 values)
- **metazone.bin**: Export config creates this file on USB (menu 304)
**Notes**: Critical for proper touchscreen calibration and touch button mapping. "nokey" indicates unassigned/empty touch areas. X/Y axis swap fixes reversed/mirrored touch coordinates. GtpAdbTool provides advanced calibration using /proc config data. Factory reset may require recalibration.

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
