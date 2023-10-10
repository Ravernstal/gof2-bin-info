# ships.bin - Ships

`ships.bin` contains a list of ships and their attributes.
Each entry has the following format:

| Size (Bytes) | Data Type | Name | Notes |
| --- | --- | --- | --- |
| 4 | Integer | Ship ID | |
| 4 | Integer | Armour rating | |
| 4 | Integer | Cargo capacity | |
| 4 | Integer | Price | |
| 4 | Integer | Primary weapon count | |
| 4 | Integer | Secondary weapon count | |
| 4 | Integer | Turret count | The game does not support more than 1 turret per ship |
| 4 | Integer | Equipment slot count | |
| 4 | Integer | Handling | |

## Notes

* The ships with IDs 13, 14, and 15 are the Vossk freighter, Terran battlecruiser, and Nivelian freighter respectively.
* All three of these have the exact same stats according to the file.
* In order to play as these ships, new entries need to be added to [weapons*.bin](weapons.md).
* Ship names can be found in the lang files starting at index 913.
* There are 64 ships defined in this file.
* This file is big-endian.
