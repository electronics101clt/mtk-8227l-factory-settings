# Documentation Workflow

Step-by-step process for documenting MTK 8227L factory settings menus.

## Prerequisites

- ADB connected to MTK 8227L device
- Access to factory settings (password 8888)
- XDA Forums access for research

## Workflow Steps

### 1. Take Screenshot
```bash
adb exec-out screencap -p > /tmp/menu_current.png
```

### 2. Read Screenshot
Identify menu contents:
- Menu title/number
- All options and settings
- Current values
- Buttons and controls
- Any dialog messages

### 3. Search XDA Forums
Research the menu using multiple search queries:
- `8227L [menu name] XDA`
- `8227L "[specific text from menu]" factory settings`
- `MTK 8227L [feature] XDA forums`

### 4. Update MENU-REFERENCE.md
Document findings in the menu entry:

```markdown
### [XXX] - [Menu Name]
**Status**: ✅ Documented
**Purpose**: [What this menu does]
**Interface**: [Description of UI elements]
**Settings**:
- **[Setting 1]**: [Description and current value]
- **[Setting 2]**: [Description and current value]
**Buttons**:
- **[Button 1]**: [What it does]
**XDA References**:
- [Key finding from XDA search]
- [Related thread information]
**Notes**: [Additional context, warnings, hardware requirements, etc.]
```

### 5. Commit to Git
```bash
git add MENU-REFERENCE.md
git commit -m "Document menu [XXX]: [Menu Name] with [key details]"
```

### 6. Delete Screenshot
```bash
rm /tmp/menu_current.png
```

### 7. Repeat
Navigate to next menu and repeat workflow.

## Remaining Menus to Document

### 100 Series (Mounting Vehicle Settings)
- 104: [Unknown - not yet accessed]
- 106: Help and Feedback

### 700 Series (Engineering Settings)
- 701: USB Settings
- 702: Clear Test File
- 703: Debug Touch
- 704: App Settings
- 705: Touch Test
- 706: Bluetooth Connect Pair Set
- 707: MCU Info Test
- 708: Engineering Test Debugging

## Tips

- **Don't waste time**: Take screencap → XDA search → update markdown → commit → dispose
- **Be thorough**: Search XDA forums extensively for each menu item
- **Document everything**: Settings, buttons, values, hardware requirements, XDA references
- **Local commits only**: Do not push to remote (user handles push)
- **No screenshots in repo**: Only use for documentation, then delete immediately

## XDA Search Resources

- [8227L android unit 8.1 chinese](https://xdaforums.com/t/8227l-android-unit-8-1-chinese.3905535/) - Main discussion
- [ALPS FF5000 & other headunits (8227L) pin codes](https://xdaforums.com/t/alps-ff5000-other-headunits-8227l-pin-codes-for-factory-menus.4269431/) - PIN codes
- [Collection of 8227l firmware](https://xdaforums.com/t/collection-of-8227l-firmware-android-vers-6-9.4003935/) - Firmware collection
- [How to access Engineering Mode for AC8227L](https://xdaforums.com/t/how-to-access-engineering-mode-for-ac8227l.4592425/) - Access codes

## Command to Continue

User will say: **"screencap and repeat workflow"**

This triggers the automated workflow for the next menu in sequence.
