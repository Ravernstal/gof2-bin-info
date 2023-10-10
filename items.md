# items.bin - Items

`items.bin` contains a list of items, their attributes, and their blueprint ingredients (if they are a blueprint item).
Each entry consists of three lists.
The first is a list of item IDs used to create this item from a blueprint (if this item is not a blueprint item, this list will be empty and the length will be zero).
The second is a list of blueprint item counts, each corresponding to the item ID in the previous list (again, if this is not a blueprint item, this list will be empty).
The final list is a list of key-value pairs where each key corresponds to an attribute ID, and the value is the value for that attribute.
The format of each item entry is as follows:

| Size (Bytes) | Data Type | Name | Notes |
| --- | --- | --- | --- |
| 4 | Integer | Number of blueprint item IDs (`b`) | |
| 4 x `b` | Integer | Blueprint item IDs | |
| 4 | Integer | Number of blueprint item counts (`c`) | |
| 4 x `c` | Integer | Blueprint item counts | |
| 4 | Integer | Number of attributes and values (`a`) | |
| 4 x `a` | Integer | Attribute ID / value (alternating) | e.g. if this list had a length of 8, it would have 4 attributes and 4 corresponding values in the format `avavavav` |

The known attributes IDs are as follows:

| ID | Name | Notes |
| --- | --- | --- |
| 0 | Index | Item ID |
| 1 | Type | |
| 2 | Sort | |
| 3 | Tech level | |
| 4 | Minimum price system ID | System ID where the price is at its lowest |
| 5 | Maximum price system ID | System ID where the price is at its highest |
| 6 | Occurence % | |
| 7 | Minimum price | |
| 8 | Maximum price | |
| 9 | Damage (weapon) | |
| 10 | EMP Damage (weapon) | |
| 11 | Loading speed ms (weapon) | |
| 12 | Shot lifetime ms (weapon) | |
| 13 | Speed factor (weapon) | |
| 14 | Magnitude m (secondary weapon) | |
| 15 | Steerable? (secondary weapon) | Value of 0x0 = false, 0x1 = true |
| 16 | Automatic? (turret) | Value of 0x0 = false, 0x1 = true |
| 17 | Handling (turret) | |
| 18 | Capacity (shield) | |
| 19 | Loading speed ms (shield) | |
| 20 | Armour (armour) | |
| 22 | Effect % (compressor) | |
| 23 | Automatic? (tractor beam) | Value of 0x0 = false, 0x1 = true |
| 24 | Lock time ms (tractor beam) | |
| 25 | Effect % (booster) | |
| 26 | Loading speed ms (booster) | |
| 27 | Duration ms (booster) | |
| 28 | Effect % (thruster) | |
| 29 | Lock time ms (scanner) | |
| 30 | Show class A asteroids? (scanner) | Value of 0x0 = false, 0x1 = true |
| 31 | Show cargo? (scanner) | Value of 0x0 = false, 0x1 = true |
| 32 | Handing % (drill) | |
| 33 | Yield % (drill) | |
| 34 | Size (cabin) | |
| 35 | Effect ms (cloak) | |
| 36 | Loading speed ms (cloak) | |
| 37 | Loading speed ms (Khador drive) | |
| 38 | Energy consumption (cloak/Khador drive) | |
| 39 | Fire rate % (weapon mod) | |
| 40 | Damage % (weapon mod) | |
| 41 | Effect ms (emergency system) | |
| 42 | Effect ms (time extender) | |
| 43 | Loading speed ms (time extender) | |
| 50 | Magnitude (plasma collector) | |
| 52 | Capacity (gamma shield) | |
| 53 | Range (repair beam) | |
| 54 | Effect (repair beam) | |
| 55 | Count (repair beam) | |
| 56 | Effect (ion missile) | |
| 57 | Show info? (spectral filter) | Value of 0x0 = false, 0x1 = true |
| 58 | Show on radar? (spectral filter) | Value of 0x0 = false, 0x1 = true |
| 59 | Consumption (shield injector) | |
| 60 | Vossk item? | Value of 0x0 = false, 0x1 = true |

## Notes

* Item names can be found in the lang files starting at index 1274.
* There are 233 items defined in this file.
* This file is big-endian.
