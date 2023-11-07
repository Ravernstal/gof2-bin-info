# ticker.bin - News Items

`ticker.bin` contains a list of news ticker items.
These appear at the bottom of the hangar screen, and can change depending on the current story mission.
Each entry has the following format:

| Size (Bytes) | Data Type | Name | Notes |
| --- | --- | --- | --- |
| 4 | Boolean | Unknown | Either 0x0 or 0x1 |
| 4 | Boolean | Show in Terran systems | Either 0x0 or 0x1 |
| 4 | Boolean | Show in Vossk systems | Either 0x0 or 0x1 |
| 4 | Boolean | Show in Nivelian systems | Either 0x0 or 0x1 |
| 4 | Boolean | Show in Midorian systems | Either 0x0 or 0x1 |
| 4 | Integer | Start mission ID | The ID of the first story mission that this news item will appear during |
| 4 | Integer | End mission ID | The ID of the last story mission that this news item will appear during |

## Notes

* There are 59 news items defined in this file.
* This file is big-endian.
