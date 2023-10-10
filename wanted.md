# wanted.bin - Most Wanted

`wanted.bin` contains a list of most wanted characters.
Each entry has the following format:

| Size (Bytes) | Data Type | Name | Notes |
| --- | --- | --- | --- |
| 2 | Integer | Name length (`n`) | |
| `n` | String | Name | UTF-8 encoded |
| 4 | Integer | Most wanted ID | |
| 4 | Integer | Board faction | 0x0 = Terran, 0x1 = Vossk, 0x2 = Nivelian, 0x3 = Midorian |
| 4 | Integer | Race | 0x0 = Terran, 0x1 = Vossk, 0x2 = Nivelian, 0x3 = Midorian |
| 4 | Integer | Unknown | Always 0x1 |
| 4 | Integer | Ship ID | Ships are defined in [ships.bin](ships.md) |
| 4 | Integer | Weapon item ID | Items are defined in [items.bin](items.md) |
| 4 | Integer | HP | |
| 4 | Integer | Loot item ID | Items are defined in [items.bin](items.md) |
| 4 | Integer | Loot amount | |
| 4 | Integer | Reward | Credits |
| 4 | Integer | Number of bounties required | |
| 4 | Integer | Required mission ID | |
| 4 | Integer | Number of wingmen | |
| 4 | Integer | Number of image parts (`n`) | Always 5 |
| 4 x `n` | Integer | Image part ID | |

## Notes

* There are 25 entries defined in this file.
* This file is big-endian.
