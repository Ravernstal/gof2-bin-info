# names_*.bin - Names

The `names_*.bin` files contain lists of names for people in space lounges.
Each file has a 4 byte header which indicates the number of entries, and each entry has the following format:

| Size (Bytes) | Data Type | Name | Notes |
| --- | --- | --- | --- |
| 2 | Integer | Name length (`n`) | |
| `n` | String | Name | UTF-8 encoded |

## Notes

* These files are big-endian.
