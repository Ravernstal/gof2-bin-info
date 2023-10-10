# weapons*.bin - Ship Weapon/Engine Positions

`weapons*.bin` contains a list of primary, secondary, turret, and thruster positions per ship.
Each entry has the following format:

| Size (Bytes) | Data Type | Name | Notes |
| --- | --- | --- | --- |
| 2 | Integer | Ship ID | |
| 2 | Integer | Number of positions | |
| Variable | Position | Position | |

Each position has the following format:

| Size (Bytes) | Data Type | Name | Notes |
| --- | --- | --- | --- |
| 2 | Integer | Position type | 0x0 = primary weapon, 0x1 = secondary weapon, 0x2 = turret, 0x3 = engine |
| 2 | Integer | X position | |
| 2 | Integer | Y position | |
| 2 | Integer | Z position | |

If the position type is 0x3 (an engine), then the following fields will also be included:

| Size (Bytes) | Data Type | Name | Notes |
| --- | --- | --- | --- |
| 4 | Float | Engine intensity (X) | All three of these values control the size of the flame. Oddly, they are always equal and the game seems to use the lowest value of the three |
| 4 | Float | Engine intensity (Y) | |
| 4 | Float | Engine intensity (Z) | |

## Notes

* There are 59 entries defined in this file.
* This file is little-endian.
