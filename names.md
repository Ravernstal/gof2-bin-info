# names_*.bin

The `names_*.bin` files contain lists of names for people in space lounges. Each file has a 4 byte header which indicates the number of entries, and each entry has the following format:

| Size | Name | Description |
| --- | --- | --- |
| 1 byte | Separator | Always 0x0 |
| 1 byte | Name length | |
| Variable | Name | In UTF-8 format |
