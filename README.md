# Weapon Limits Adjuster

The game has a hardcoded limit on the number of weapons.meta files that can be loaded and on the total number of weapon components that can be defined, which Rockstar increases everytime new weapons.meta or weapon components are added in DLCs.

Reaching any these limits when installing weapon mods makes the game crash while loading. This ASI allows you to increase these limits to prevent those crashes.

## Installation

Install an ASI loader (dinput8.dll).
Then, just drop `WeaponLimitsAdjuster.asi` and `WeaponLimitsAdjuster.ini` in your GTAV directory.

If you have installed the old version and still have `CWeaponInfoBlob Adjuster.asi` and `CWeaponInfoBlob Adjuster.ini` in your GTAV directory, **delete them**. Otherwise, both ASIs will conflict and crash.

## Configuration

The `WeaponLimitsAdjuster.ini` file allows you define the new limits. It has two settings:

- `CWeaponInfoBlob`: determines the maximum number `weapons.meta` files that can be included in the game files (default: 512).
- `CWeaponComponentInfo`: determines the maximum total number of weapon components that can be defined in `weaponcomponents.meta` files. **Important**: the pool size `CWeaponComponentInfo` in gameconfig.xml should have the same value, otherwise the game will crash when the number of weapon components reaches this pool size (default: 1024).
