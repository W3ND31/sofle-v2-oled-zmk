# TODO List - Sofle V2 RGB with Dongle

This file contains planned tasks for future firmware improvements and optimizations.

## 🔋 Power Management

### 🔍 Optimize Battery Code for 2000 mAh Batteries
**Status**: 🔴 Pending  
**Priority**: Medium  
**Description**: Investigate and optimize code related to managing the 2000 mAh batteries on the left and right keyboard sides to maximize battery life.

**Aspects to investigate**:
- Review current `CONFIG_ZMK_BATTERY` settings
- Check if there are specific configurations for higher capacity batteries
- Analyze battery sensor polling rate
- Optimize battery level update frequency
- Investigate voltage divider settings if applicable
- Review deep sleep and idle timeout configurations
- Compare current consumption with benchmarks from similar projects
- Consider disabling non-essential features when battery is low

**Current settings to review**:
- `CONFIG_ZMK_SPLIT_BLE_CENTRAL_BATTERY_LEVEL_FETCHING=y`
- `CONFIG_ZMK_SPLIT_BLE_CENTRAL_BATTERY_LEVEL_PROXY=y`
- Battery polling frequency
- Nice!Nano v2 power profile configurations

**Required tests**:
- Measure actual current consumption in different states (active, idle, deep sleep)
- Calculate theoretical vs actual battery duration
- Test different RGB configurations and their impact on battery
- Monitor consumption during active BLE connection

**References**:
- [ZMK Battery Configuration](https://zmk.dev/docs/config/battery)
- [Nice!Nano Power Consumption](https://nicekeyboards.com/docs/nice-nano/pinout-schematic)
- Documentation for the specific battery hardware used

---

## 📝 General Notes

### Recent Changes Implemented ✅
- ✅ RGB Underglow configured on all devices (central, left, right)
- ✅ RGB auto-off when idle
- ✅ ZMK Studio enabled
- ✅ Mouse support enabled
- ✅ 7 BT connections configured (2 peripherals + 5 hosts)
- ✅ OLED display SH1106 working on central dongle
- ✅ Encoders configured on left/right sides
- ✅ Battery level proxy through central dongle
- ✅ Online keymap editor configured
- ✅ Deep sleep implemented (1 min idle, 30 min deep sleep on sides; 3h on dongle)

### How to Contribute
If you want to add new items to this list or work on any existing items, feel free to:
1. Create a branch with the feature name
2. Implement and test the changes
3. Update this file marking the item as completed
4. Make a commit with a detailed description

---

**Last updated**: November 21, 2025
