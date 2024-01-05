# *.lang - Language Strings

The `*.lang` files contain lists of strings used throughout the game.
Each file has series of entries, each of which has the following format:

| Size (Bytes) | Data Type | Name | Notes |
| --- | --- | --- | --- |
| 2 | Integer | Text length (`n`) | |
| `n` | String | Text | UTF-8 encoded |

## Notes

* These files are big-endian.
