# agents.bin - Agents

`agents.bin` contains a list of agents (people who sell system coordinates, blueprints, and modifications in space lounges). 
Each entry has the following format:

| Size (Bytes) | Data Type | Name | Notes |
| --- | --- | --- | --- |
| 2 | Integer | Name length (`n`) | |
| `n` | String | Name | UTF-8 encoded |
| 4 | Integer | Agent ID | |
| 4 | Integer | Station ID | |
| 4 | Integer | System ID | |
| 4 | Integer | Race | 0x0 = Terran, 0x1 = Vossk, 0x2 = Nivelian, 0x3 = Midorian |
| 4 | Boolean | Is male | Either 0x0 or 0x1 |
| 4 | Integer | Sell system ID | The system ID of the system being sold, or -1 if none. Systems are defined in [systems.bin](systems.md). Each agent may only sell one type of item |
| 4 | Integer | Sell blueprint ID | The item ID of the blueprint being sold, or -1 if none. Items are defined in [items.bin](items.md) |
| 4 | Integer | Sell mod ID | The modification ID of the mod being sold, or -1 if none |
| 4 | Integer | Sell price | |
| 4 | Integer | Number of image parts (`n`) | Always 5 |
| `n` | Integer | Image part ID | |

## Notes

* There are 13 agents defined in this file.
* This file is big-endian.
