# gof2_save_game_preview_* - Save Game Preview

`gof2_save_game_preview_*` contains some basic information about a save game which is displayed on the load game menu.
This information has the following format:

| Size (Bytes) | Data Type | Name | Notes |
| --- | --- | --- | --- |
| 8 | Integer | Play time (ms) | |
| 4 | Integer | Credits | |
| 4 | Integer | Station name length (`a`) | |
| `a` | String | Station name | UTF-16 encoded |
| 4 | Integer | System name length (`y`) | |
| `y` | String | System name | UTF-16 encoded |
| 4 | Integer | Campaign mission ID | |
| 4 | Integer | Level | |
| 4 | Float | Difficulty | |
| 4 | Integer | Ship ID | Ships are defined in [ships.bin](ships.md) |

## Notes

* This file is little-endian.
