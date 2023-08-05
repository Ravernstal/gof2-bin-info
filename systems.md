# systems.bin

`systems.bin` contains a list of solar systems in the game. Each entry has the following format:

| Size | Name | Description |
| --- | --- | --- |
| 1 byte | Separator | Always 0x0 |
| 1 byte | Name length | |
| Variable | Name | In UTF-8 format |
| 4 bytes | Risk level | 0x0 = dangerous, 0x1 = risky, 0x2 = average, 0x3 = secure |
| 4 bytes | Unlocked at start | Whether or not the system is visible at the start of the game. Either 0x0 or 0x1 |
| 4 bytes | Faction | 0x0 = Terran, 0x1 = Vossk, 0x2 = Nivelian, 0x3 = Midorian |
| 4 bytes | Map X coordinate | |
| 4 bytes | Map Y coordinate | |
| 4 bytes | Map Z coordinate | |
| 4 bytes | Jumpgate station ID | Station ID of the planet with a jumpgate, or 0xFFFFFFFF for systems without one e.g. Mido |
| 4 bytes | Star colour ID | 0x0 = green, 0x9 = white |
| 4 bytes | Unknown | Always 0x3, maybe a list size? |
| 4 bytes | Unknown | |
| 4 bytes | Unknown | |
| 4 bytes | Unknown | |
| 4 bytes | Planet/station count | No system in the game has more than 5 stations |
| 4 bytes per entry | Station ID | |
| 4 bytes | Linked systems count | |
| 4 bytes per entry | System ID | Make sure to link systems both ways |
| 4 bytes | Unknown | Always 0x3, maybe a list size? Code references this data as "forbidden goods". |
| 4 bytes | Unknown | Always 0x0 |
| 4 bytes | Unknown | Always 0x1 |
| 4 bytes | Unknown | Always 0x2 |
