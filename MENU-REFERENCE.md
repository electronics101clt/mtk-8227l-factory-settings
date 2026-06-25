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
**Status**: ✅ Documented
**Purpose**: Export/backup system configuration to USB drive
**Interface**: Export data settings screen with adjustable parameters
**Settings Shown Before Export**:
- **Media Volume**: Default 30 (adjustable with +/- buttons)
- **Call Volume**: Default 30 (adjustable with +/- buttons)
- **Language**: English (selectable with arrows)
- **Bluetooth Name**: CarBT (editable)
- **Bluetooth pwd**: 0000 (editable)
**Output File**: Creates **metazone.bin** on USB drive (1MB file)
**File Contents**: Motherboard-specific settings including:
- Button mappings
- Touch panel configuration
- Screen configuration
- Volume levels
- Language settings
- Bluetooth configuration
**Requirements**: USB drive must be inserted (message shows "Not inserted U disk" if missing)
**XDA References**:
- Creates metazone.bin file on USB drive (1MB)
- Contains motherboard-specific settings (button, touch, screen configs)
- Used for backup/restore when flashing firmware
- Recommended to backup and flash your own metazone.bin with different firmware
- Related to PIN code 5555 for advanced settings export
- File can be checked with hex editor but may appear mostly empty
- Used in USB firmware flashing process along with 8227L-8.upd, logo.bin, preloader.bin
**Notes**: Critical for preserving custom configurations when updating firmware. metazone.bin contains device-specific calibration and settings. Always backup before flashing new firmware. File placed in root of USB drive.

### 305 - Direction Control Settings
**Status**: ✅ Documented
**Purpose**: Steering wheel control KEY1/KEY2 input resistor configuration
**Interface**: Radio button selection screen with two setting rows
**Settings**:
- **Direction control key value ranges**:
  - Level one
  - Level two (selected in screenshot)
  - Level three
  - Level Four
  - **Purpose**: Sensitivity/detection levels for steering wheel control button recognition
- **PullUpSelection**:
  - FixedPullUp_10K (10kΩ fixed pull-up resistor)
  - VariablePullUp (selected in screenshot) - Auto-detecting pull-up
  - FixedPullUp_0.47K (470Ω fixed pull-up resistor)
  - **Purpose**: Configure pull-up resistor value for KEY1/KEY2 inputs
**OK Button**: Save configuration
**XDA References**:
- Factory settings menu (password 8888) has 1K/10K/20K setting for max resistor values
- KEY1 input expects 0-1K Ohms for button detection
- Steering wheel controls connect KEY1 to ground using resistor arrays
- Resistor values act as voltage divider to detect which button is pressed
- Different vehicles use different resistor values for steering wheel controls
- VariablePullUp allows auto-detection of vehicle's resistor scheme
**Notes**: **NOT related to navigation bar orientation** (originally suspected purpose). This menu configures steering wheel control hardware interface. Direction = steering wheel control direction (not screen direction). Level one-four = sensitivity levels for resistor-based button detection. PullUpSelection matches pull-up resistor to vehicle's steering wheel control resistor array. FixedPullUp_10K for high resistance vehicles, FixedPullUp_0.47K for low resistance vehicles, VariablePullUp for automatic detection.

### 306 - IR Code Output Settings
**Status**: ✅ Documented
**Purpose**: Configure infrared (IR) remote control protocol for steering wheel controls
**Interface**: System Info Config Settings screen with protocol selection
**Options**:
- **IR protocol output** (selected in screenshot) - Generic IR protocol mode
- **NEC protocol output** - NEC infrared protocol (standard consumer electronics IR protocol)
**Buttons**:
- **OK**: Save protocol selection
- **Send**: Send/test IR codes
**Status Display**: "No profile" - indicates no IR codes have been learned/configured yet
**XDA References**:
- 8227L primarily uses analog KEY1/KEY2 resistive inputs (not IR-based)
- IR remote option available as alternative to resistive steering wheel controls
- Learnable IR remote control accessories attach to steering wheel (under $10)
- Units feature "KEY learning" or "Steering Wheel Learning" option to program IR codes
- NEC protocol is standard IR protocol used in consumer electronics
- Some YT9217 variants do not support IR remote functionality
- IR remotes use learning/programming approach (not pre-programmed codes)
- Modern vehicles with factory steering wheel controls need Connects2-style adaptor
**Protocol Details**:
- **NEC Protocol**: Standard infrared remote control protocol, pulse distance encoding
- **IR protocol output**: Generic IR mode (may support multiple protocol types)
- Learning mode allows programming custom IR codes to head unit functions
**Notes**: Alternative to resistive KEY1/KEY2 steering wheel controls (menu 305). Allows using learnable IR remote controls instead of hardwired resistive controls. "No profile" indicates codes need to be learned via KEY learning mode in settings. NEC is industry-standard IR protocol. Used primarily when vehicle steering wheel controls are not compatible with resistive KEY1/KEY2 interface.

### 307 - Encoder Settings
**Status**: ✅ Documented
**Purpose**: Rotary encoder (volume knob) hardware detection and configuration
**Interface**: Settings screen with encoder detection method and direction configuration
**Settings**:
- **Encoder reading ways**:
  - **I/0 detect** (selected in screenshot) - Digital I/O quadrature encoder detection
  - **AD detect 1** - Analog-to-digital detection method 1
  - **AD detect 2** - Analog-to-digital detection method 2
  - **AD detect 3** - Analog-to-digital detection method 3
- **Encoder 1 setting**:
  - **positive direction** (selected) - Clockwise rotation increases volume
  - **negative direction** - Clockwise rotation decreases volume (reversed)
  - **Knob AD1 Off** - Disable encoder 1 analog detection
- **Encoder 2 setting**:
  - **positive direction** (selected) - Clockwise rotation increases volume
  - **negative direction** - Clockwise rotation decreases volume (reversed)
  - **Knob AD2 Off** - Disable encoder 2 analog detection
- **Encoder 1 and Encoder 2 Functions Swap**: Checkboxes to swap encoder functions
  - **Message**: "AD is not input values" (shown when not using AD detection mode)
**OK Button**: Save configuration
**Detection Methods**:
- **I/0 detect**: Digital quadrature encoder (two-channel A/B phase detection)
- **AD detect 1/2/3**: Analog-to-digital detection using resistor ladder/voltage divider
**XDA References**:
- Common issue: After crash/reboot, unit doesn't recognize volume knob ("key study fail")
- Volume knob requires specific key.ini file from seller
- Firmware update from seller can fix volume knob recognition issues
- Different hardware variants use different encoder types (quadrature vs analog)
- Factory settings (password 8888) allows encoder configuration
- Units may have firmware for volume knob variant vs touchscreen-only variant
**Notes**: Configures hardware detection method for rotary volume encoder. I/O detect = standard quadrature encoder (most common). AD detect = analog detection using resistor network. Positive/negative direction determines if clockwise rotation increases or decreases volume. Swap function allows reversing encoder assignments. Common issues require seller-specific key.ini file or firmware update to fix encoder recognition after system crash.

### 308 - Physical Buttons Study
**Status**: ✅ Documented
**Purpose**: Learn and map physical buttons to head unit functions
**Interface**: Grid layout with button function assignments and "Key AD value" header
**Button Functions Available**:
- **Row 1**: power, voladd, voldec, prev
- **Row 2**: next, play/pause, mute, aps
- **Row 3**: menu, mode, back, radio
- **Row 4**: music(Optional), navi, hangup, phone
- **Row 5**: screen on/off→, blooth→, seek+→, seek-→
- **Row 6**: Lights, FM→, AM→, multiplexing→
- **Row 7**: start, key in and out, other, clear
**Controls**:
- **start**: Begin button learning/mapping process
- **key in and out**: Import/export button configurations
- **other**: Other/custom button functions
- **clear**: Clear/reset button mappings
**Learning Process**:
1. Click "start" to begin
2. Select button name on screen (e.g., home, power, voladd, voldec)
3. Press corresponding physical button on unit
4. Shows X/Y coordinates or AD (analog-digital) value for button
5. Must complete all buttons in one session
6. Save configuration when done
**XDA References**:
- Access via Car Settings → Factory Settings → password 8888 → Physical button study
- Alternative access: password 1234 or 000000 on some units
- "Knob panel button learning" feature works even for units with buttons (not knobs)
- Allows short press and long press actions for same button (up to 8 functions vs 4)
- Process: Delete current key → hold map key → press physical button simultaneously
- Software "studies" by selecting function on screen, then pressing physical button
- Some units write-protected by seller (cannot remap)
- Common issue: After logo change, side buttons stop working, remapping has no effect
- Some variants (Avison N8) have touch study only, no button study
- Config file may show "config file not found" error on some units
**Key AD value**: Shows analog-digital voltage value for resistive button detection
**Notes**: Critical for configuring panel buttons after firmware changes or when buttons stop working. Button assignments use AD (analog-digital) values from resistor network. Supports both momentary functions and toggle functions. Arrow symbols (→) indicate additional/advanced functions. Some units may be locked by manufacturer preventing remapping.

### 309 - Tire Pressure Settings
**Status**: ✅ Documented
**Purpose**: Configure TPMS (Tire Pressure Monitoring System) alarm thresholds
**Interface**: Slider-based configuration screen for tire pressure and temperature limits
**Settings**:
- **Left front tire Pressure setting**:
  - upper: 270 (kPa or PSI) - high pressure alarm threshold
  - lower: 170 (kPa or PSI) - low pressure alarm threshold
- **Left rear tire Pressure setting**:
  - upper: 270 (kPa or PSI) - high pressure alarm threshold
  - lower: 170 (kPa or PSI) - low pressure alarm threshold
- **Right front tire Pressure setting**:
  - upper: 270 (kPa or PSI) - high pressure alarm threshold
  - lower: 170 (kPa or PSI) - low pressure alarm threshold
- **Right back tire Pressure setting**:
  - upper: 270 (kPa or PSI) - high pressure alarm threshold
  - lower: 170 (kPa or PSI) - low pressure alarm threshold
- **Alarm temperature setting**:
  - upper: 65°C - high temperature alarm threshold
**Buttons**:
- **OK**: Save TPMS configuration
- **default**: Reset to factory default values (270/170 pressure, 65°C temperature)
**XDA References**:
- TPMS listed as optional feature on MTK 8227L VW head units
- Advanced configurations accessible via code 8888
- Custom firmware (YT9216B) includes TPMS functionality with cheap Chinese USB units
- Some units have Bluetooth Low Energy TPMS sensor compatibility issues (requires Bluetooth 4.0)
- TPMS typically add-on feature, not standard on all 8227L units
- USB TPMS systems work with Android head units (Chinese language notification issues on some)
**TPMS System Details**:
- Monitors tire pressure and temperature in real-time
- Transmits statistics to receiver/head unit
- Sounds warning alarm when parameters exceeded
- Custom upper/lower limit alarm values
- May use USB dongle or Bluetooth 4.0 sensors
- Integration via CAN or LIN protocols on some vehicles
**Notes**: Configures alarm thresholds for external TPMS sensor system. Values 270/170 likely PSI or kPa (check sensor documentation). Temperature alarm at 65°C protects against overheating tires. Requires compatible TPMS sensor hardware (USB dongle or Bluetooth 4.0 sensors). Not all 8227L units include TPMS functionality - may require specific firmware variant or hardware.

### 310 - Lock Screen Mode Settings
**Status**: ✅ Documented
**Purpose**: Configure lock screen display mode when unit enters standby
**Interface**: Two-option radio button selection
**Options**:
- **Time mode**: Display clock/time/date when unit is in standby (screen shows time when ACC power off)
- **Screen off mode** (default/selected): Turn screen completely off when unit enters standby
**Buttons**:
- **OK**: Save lock screen mode configuration
**Behavior**:
- **Time mode**: When power button pressed or ACC turned off, screen displays time/date information (standby clock display)
- **Screen off mode**: When power button pressed or ACC turned off, screen turns completely off (no display)
**Related Settings**:
- Standby time setting available in Common menu
- Display backlight settings control daytime/nighttime brightness
- Related to ACC (accessory power) behavior when ignition turned off
**XDA References**:
- Older Android car radios had sleep mode option when ACC off
- 8227L units: 4PDA forum discussions indicate shutdown delay feature not available
- Lock screen timeout issues reported (86200 second countdown on some units)
- Cold boot problematic on some firmware versions
**Notes**: Controls what happens to screen display when unit enters standby/ACC off state. Time mode shows clock for quick time check without starting full system. Screen off mode saves power and reduces distraction. Setting typically persists across power cycles. Factory default is screen off mode.

### 311 - Key Light Settings
**Status**: ✅ Documented
**Purpose**: Configure RGB LED backlight for physical buttons
**Interface**: RGB color sliders with brightness and flicker controls
**Settings**:
- **red**: RGB red channel (0-255) - currently 0
- **green**: RGB green channel (0-255) - currently 0
- **blue**: RGB blue channel (0-255) - currently 0
- **Brightness level**: Overall LED brightness (0-100%) - currently 100
- **flicker frequency**: PWM flicker rate for LED dimming (0-100) - currently 0
**Color Palette**: Quick selection buttons (red, orange, yellow, green, indigo, blue, white)
**Dialog**: "Please open the debug button lamp lights!!" - appears when accessing RGB controls
**Hardware Limitations**:
- **RGB error message**: "Please open the debug button lamp lights!!" indicates RGB controller NOT fitted to unit
- **Budget units**: Only white LEDs installed (no RGB hardware), RGB settings non-functional
- **Premium units**: True RGB LEDs available on higher-end 8227L models
- Manufacturer cost-cutting: RGB controller and RGB LEDs omitted on cheaper units
**XDA References**:
- Accessed via factory settings code 8888 → Key light settings
- RGB slider available but only works on units with RGB LED hardware
- Budget units have white-only LEDs despite RGB controls appearing in menu
- Some units have 3 checkboxes below slider: keep lights on option, flicker option, third unknown
- Settings may not persist after Magisk rooting on some units
- Can deselect "open light" to disable LEDs during daytime
- Lights typically auto-activate with car headlights (connected to illumination wire)
**Flicker Frequency**:
- Controls PWM (Pulse Width Modulation) frequency for LED brightness control
- Lower values = slower flicker (may be visible)
- Higher values = faster flicker (smoother dimming)
- Setting 0 = no PWM flicker (full DC brightness control)
**Notes**: RGB color mixing only functional on premium units with actual RGB LED hardware. Budget units display RGB controls but only have white LEDs. "Debug button lamp lights" error = hardware limitation, not fixable in software. Brightness level and flicker frequency should work on all units. Color palette provides quick presets. Checkboxes below sliders control auto-on behavior and flicker enable/disable.

---

## Engineering Settings (700 Series)

### 701 - USB Settings
**Status**: ✅ Documented
**Purpose**: Audio configuration and USB-related settings interface
**Interface**: Multi-page settings menu with sidebar navigation (Audio/Logo/Other)
**Access**: Engineering Settings (700 series) → 701

#### Audio Sidebar - Volume Page
**Interface**: Volume slider screen with 6 independent audio channel controls
**Header Text**: "Silence all the sounds except Alarm, BackCar and BT Phone"
**Volume Channels**:
- **Media**: Media playback volume (music, video apps) - Default: 30
- **GS**: GPS/Navigation voice guidance volume - Default: 30
- **BackCar**: Backup camera audio/beep volume - Default: 30
- **Ring**: Ringtone volume (incoming calls, notifications) - Default: 30
- **Call**: Phone call volume (in-call audio) - Default: 30
- **Auxin**: Auxiliary input volume (external audio sources) - Default: 30
**Range**: 0-30 for all channels

#### Audio Sidebar - Sound Effect Page
**Interface**: EQ and audio processing controls with sliders and buttons
**Settings**:
- **Assistant**: Voice assistant volume/processing - Default: 30 (range 0-30)
- **Alternate**: Alternate audio stream volume - Default: 30 (range 0-30)
- **Bass**: Low frequency EQ control (button/slider)
- **Alto**: Mid-range/midrange frequency EQ control (button/slider)
- **Treble**: High frequency EQ control (button/slider)
- **Balance**: Left/right speaker balance (button/slider)
- **Loudness**: Loudness compensation enable/disable (button)

#### Logo Sidebar - Boot Logo Configuration
**Interface**: Boot logo/splash screen customization interface
**Buttons**:
- **Set path**: Select folder containing boot logo image (USB or internal storage)
- **Set logo**: Apply selected boot logo image to device
**Alternative Access**: PIN code 5678 opens custom boot logo window (com.ts.logoset.LogoSetMainActivity)
**Image Requirements**:
- **Format**: BMP (primary) or PNG (some units)
- **Resolution**: 1024x600 (for 7" 8227L units) - must match screen resolution
- **Location**: USB drive root → Car_Logo folder, or internal storage
- **Filename**: Some units require "android_" prefix (e.g., android_opel.png)
**Procedure**:
1. Create "Car_Logo" folder in USB drive root directory (FAT32 formatted)
2. Place boot logo BMP/PNG file (1024x600) in Car_Logo folder
3. Insert USB drive into head unit
4. Click "Set path" → select Car_Logo folder → select logo image
5. Click "Set logo" → message "Boot logo set successful" appears
6. Go to factory settings (code 8888) and reboot device
7. New boot logo displays on next startup
**Common Issues**:
- **Path loop**: Unit repeatedly asks to select path after clicking "Set logo"
  - Solution: Try BMP format instead of PNG, or use "android_" filename prefix
- **No boot animation**: Bootlogo selector app data corrupted
  - Solution: Android settings → Apps → "bootlogo selector apk" → Clear data
- **Logo doesn't appear**: Image appears under "EXT" in factory settings but not at boot
  - Solution: Ensure proper resolution (1024x600) and BMP format
**Alternative Method** (some models):
- Create folders: AutoUpdate/config on FAT32 USB drive
- Place logo image named "default_logo.bmp" or "default_logo.png"
- Insert USB and reboot from factory settings

#### Other Sidebar - USB Configuration
**Interface**: USB port protocol and DVR enhancement settings
**Settings**:
- **usb port1 protocol**: USB protocol version for port 1
  - Current: usb2_0 (USB 2.0 protocol)
  - Options: Likely usb1_1, usb2_0, usb3_0 depending on hardware
- **usb port0 protocol**: USB protocol version for port 0
  - Current: usb2_0 (USB 2.0 protocol)
  - Options: Likely usb1_1, usb2_0, usb3_0 depending on hardware
- **usb mode**: USB connection mode
  - Current: device (Android device mode - allows PC connection/ADB)
  - Options: Likely device, host, OTG
- **Engineer mode**: Access to engineering/diagnostic tools
  - Access: Factory Settings → USB Info → USB → "Engineering Mode"
  - Contains: Phone, connectivity, and audio options
**DVR Enhancement Checkboxes**:
- **USB0 DVR Enhancement**: Enable enhanced DVR/dashcam recording for USB port 0 ✓ (checked)
  - Enables USB camera recording features on USB0
  - Part of built-in Car DVR System
  - USB cameras detected as /dev/video1 or /dev/video2
- **USB1 DVR Enhancement**: Enable enhanced DVR/dashcam recording for USB port 1 ✓ (checked)
  - Enables USB camera recording features on USB1
  - Supports front/rear USB camera configurations
  - Recordings saved to GPS card/storage automatically
**DVR Functionality**:
- Built-in Car DVR System for USB camera recording
- Connect USB camera to use Car Record function
- Automatic recording to GPS card/SD storage
- Multi-camera support (front/rear) via USB0/USB1
- USB cameras may require specific firmware/drivers

**Sidebar Navigation Icons**:
- **Audio** (purple speaker icon) - Volume settings + Sound Effect pages
- **Logo** (green icon) - Boot logo/splash screen configuration
- **Other** (camera icon) - Additional settings and options

**XDA References**:
- Factory settings accessed via PIN code 8888 (advanced settings)
- Code 8877 provides access to atc_factory menu → Audio → Sound Effect → Bass/Alto/Treble
- Code 5678 opens custom boot logo window (com.ts.logoset.LogoSetMainActivity)
- Code 26959910 accesses "Engineering test debugging" password
- VOLUME section in factory menu controls all audio levels
- Some Music apps allow tone adjustments (bass/treble) but not balance/fader
- Balance only changeable in Car settings (no fader option for front/rear speakers)
- "BOOT MEMORY VOLUME RANGE" option available (set startup volume range)
- Power amplifier settings adjustable to half in factory settings
- Loudness can be completely disabled in sound effect settings
- Boot logo must be BMP format, 1024x600 resolution for 8227L_demo units
- Car_Logo folder method: Create folder on USB root, place PNG/BMP with "android_" prefix
- After setting boot logo, reboot from factory settings (code 8888) to apply
- Bootlogo selector app data must be cleared if boot animation doesn't appear
- Some newer variants (Android 13) may not support boot logo replacement
- Engineer mode access: Factory Settings → USB Info → USB → "Engineering Mode"
- Built-in Car DVR System - connect USB Camera to use Car Record function
- USB cameras detected as /dev/video1 and /dev/video2
- DVR recordings saved to GPS card automatically
- Some units require Welink option in Factory Settings to activate USB ports
- USB mode can be configured in Developer Options
**Sources**:
- [Android headunit (8227L) - call volume / radio / mic adjustment | XDA Forums](https://xdaforums.com/t/android-headunit-8227l-call-volume-radio-volume-mic-volume-adjustment-help-using-zlink-for-apple-carplay.4549393/)
- [8227L demo Volume issue | XDA Forums](https://xdaforums.com/t/8227l-demo-volume-issue.4042497/)
- [8227L Aux input volume control | XDA Forums](https://xdaforums.com/t/8227l-aux-input-volume-control-sat-nav-audio-interuption-and-ram-share.4193819/)
- [ALPS FF5000 & other headunits (8227L) pin codes | XDA Forums](https://xdaforums.com/t/alps-ff5000-other-headunits-8227l-pin-codes-for-factory-menus.4269431/)
- [Junsun V1 - Codes | XDA Forums](https://xdaforums.com/t/junsun-v1-codes.4282299/page-3)
- [Collection of 8227l firmware | XDA Forums](https://xdaforums.com/t/collection-of-8227l-firmware-android-vers-6-9.4003935/page-51)
- [AIPS 8227L Demo Audio setting problems | XDA Forums](https://xdaforums.com/t/aips-8227l-demo-audio-setting-problems.4062005/)
- [Sound parameters - 8227L demo | XDA Forums](https://xdaforums.com/t/sound-parameters-8227l-demo-generic-hu-jac_829c1_ver_0-6-tag-961al-cp-2-64gb-asp_ahd_lvds-maybe-others-as-well.4686367/)
- [8227L demo upload custom boot logo | XDA Forums](https://xdaforums.com/t/8227l-demo-upload-custom-boot-logo.4013155/)
- [Tutorial: Custom boot logo on 8227L head units | XDA Forums](https://xdaforums.com/t/tutorial-custom-boot-logo-on-8227l-head-units.4156239/)
- [How to set a new car logo on JCAC10003 and JCA8229/8227L | XDA Forums](https://xdaforums.com/t/how-to-set-a-new-car-logo-on-jcac10003-and-jca8229-8227l-models.4784722/)
- [Podofo ALPS 8227L_demo boot logo update | XDA Forums](https://xdaforums.com/t/podofo-alps-8227l_demo-boot-logo-update.4745328/)
- [How to access Engineering Mode for AC8227L | XDA Forums](https://xdaforums.com/t/how-to-access-engineering-mode-for-ac8227l.4592425/)
- [How to enable USB port in android stereo 8227l demo | XDA Forums](https://xdaforums.com/t/how-to-enable-usb-port-in-android-stereo-8227l-demo.3949112/)
- [8227L YT9216BJ Head Unit | XDA Forums](https://xdaforums.com/t/8227l-yt9216bj-head-unit.4139307/)
- [USB camera as DVR | XDA Forums](https://xdaforums.com/t/usb-camera-as-dvr.3618705/)
- [Help with USB Dashcamera | XDA Forums](https://xdaforums.com/t/help-with-usb-dashcamera.3609346/)

**Notes**: Menu 701 provides comprehensive audio, boot logo, and USB/DVR configuration despite being named "USB Settings". Contains master volume controls for all audio streams, full EQ/sound processing settings, custom boot logo upload interface, and USB port protocol configuration. GS = GPS/navigation guidance. BackCar audio preserved during silence mode for safety. Assistant/Alternate volumes control voice assistant and alternate audio stream levels. Bass/Alto/Treble provide 3-band EQ. Balance controls L/R speaker distribution. Loudness compensation boosts low frequencies at low volumes. Boot logo customization allows branding/personalization using BMP/PNG images via USB drive or internal storage. USB configuration controls protocol versions (USB 2.0) for both ports and device/host/OTG mode selection. DVR Enhancement enables built-in dashcam recording functionality using USB cameras connected to USB0/USB1 ports - recordings automatically saved to GPS card/storage. Engineer mode provides access to advanced phone/connectivity/audio diagnostics. Related to menu 108 (Power Amplifier Settings) for overall gain control. PIN code 5678 provides direct access to boot logo window. Menu 701 is the most comprehensive settings interface with three major sidebars (Audio/Logo/Other).

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
