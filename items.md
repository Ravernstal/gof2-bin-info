# items.bin

`items.bin` contains a list of items, their attributes, and their blueprint ingredients (if they are a blueprint item).
Each entry consists of three lists.
A list in this file consists of a 4 byte length `n`, and then `n` 4 byte entries.
The first is a list of item IDs used to create this item from a blueprint (if this item is not a blueprint item, this list will be empty and the length will be zero).
The second is a list of item counts, each corresponding to the item ID in the previous list (again, if this is not a blueprint item, this list will be empty).
The final list is a list of key-value pairs.
Each key corresponds to an attribute ID, and the value is the value for that attribute.
The attributes are as follows:

| ID | Attribute Name | Description |
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
| 15 | Steerable? (secondary weapon) | 0x0 = false, 0x1 = true |
| 16 | Automatic? (turret) | 0x0 = false, 0x1 = true |
| 17 | Handling (turret) | |
| 18 | Capacity (shield) | |
| 19 | Loading speed ms (shield) | |
| 20 | Armour (armour) | |
| 22 | Effect % (compressor) | |
| 23 | Automatic? (tractor beam) | 0x0 = false, 0x1 = true |
| 24 | Lock time ms (tractor beam) | |
| 25 | Effect % (booster) | |
| 26 | Loading speed ms (booster) | |
| 27 | Duration ms (booster) | |
| 28 | Effect % (thruster) | |
| 29 | Lock time ms (scanner) | |
| 30 | Show class A asteroids? (scanner) | 0x0 = false, 0x1 = true |
| 31 | Show cargo? (scanner) | 0x0 = false, 0x1 = true |
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
| 44 | Unknown | Maybe related to a mission? Seems to roughly correspond to 0x1 = Vossk-related, 0x0 = others |
| 45 | Unknown | |

Note that attribute ID 21 is not used by any item.
