# stations.bin - Planets/Space Stations

`stations.bin` contains a list of planets/space stations in the game.
Each entry has the following format:

| Size (Bytes) | Data Type | Name | Notes |
| --- | --- | --- | --- |
| 2 | Integer | Name length (`n`) | |
| `n` | String | Name | UTF-8 encoded |
| 4 | Integer | Station ID | |
| 4 | Integer | System ID | Systems are defined in [systems.bin](systems.md). |
| 4 | Integer | Tech level | 1-10 |
| 4 | Integer | Planet background ID | |

In versions of the game which have both the Valkyrie and Supernova DLCs, there are 135 stations defined in this file.
This file is big-endian.
