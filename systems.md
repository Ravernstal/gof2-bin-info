# systems.bin - Solar Systems

`systems.bin` contains a list of solar systems in the game.
Each entry has the following format:

| Size (Bytes) | Data Type | Name | Notes |
| --- | --- | --- | --- |
| 2 | Integer | Name length (`n`) | |
| `n` | String | Name | UTF-8 encoded |
| 4 | Integer | Risk level | 0x0 = dangerous, 0x1 = risky, 0x2 = average, 0x3 = secure |
| 4 | Boolean | Unlocked at start | Whether or not the system is visible at the start of the game. Either 0x0 or 0x1 |
| 4 | Integer | Faction | 0x0 = Terran, 0x1 = Vossk, 0x2 = Nivelian, 0x3 = Midorian |
| 4 | Integer | Map X coordinate | |
| 4 | Integer | Map Y coordinate | |
| 4 | Integer | Map Z coordinate | |
| 4 | Integer | Jumpgate station ID | Station ID of the planet with a jumpgate, or 0xFFFFFFFF (-1) for systems without one e.g. Mido. Stations are defined in [stations.bin](stations.md) |
| 4 | Integer | Star colour ID | 0x0 = green, 0x9 = white |
| 4 | Integer | Unknown array length (`a`) | Always 0x3 |
| 4 x `a` | Integer | Unknown | |
| 4 | Integer | Number of planets/stations (`p`) | No system in the game has more than 5 planets. |
| 4 x `p` | Integer | Station ID | Stations are defined in [stations.bin](stations.md) |
| 4 | Integer | Number of linked systems (`s`) | |
| 4 x `s` | Integer | System ID | Systems should be linked both ways |
| 4 | Integer | Unknown array length (`b`) | Always 0x3 |
| 4 x `b` | Integer | Unknown | Always 0x0, then 0x1, then 0x2 |

## Notes

* There are 34 systems defined in this file.
* This file is big-endian.
