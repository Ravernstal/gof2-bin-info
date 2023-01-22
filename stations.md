# stations.bin

`stations.bin` contains a list of planets/space stations in the game. Each entry has the following format:

| Size | Name | Description |
| --- | --- | --- |
| 1 byte | Separator | Always 0x0 |
| 1 byte | Name length | |
| Variable | Name | In UTF-8 format |
| 4 bytes | Station ID | |
| 4 bytes | System ID | |
| 4 bytes | Tech level | |
| 4 bytes | Planet background | |
