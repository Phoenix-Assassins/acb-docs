OSDK news service likely implemented by Ubisoft after taking over Quazal Technologies.

| Method ID | Method Name |
|---|---|
| 1 | [GetNewsChannel](#1-getnewschannel) |

# (1) GetNewsChannel
## Request
This method does not take any parameters.

## Response

| Type | Name |
|--|--|
| [NewsChannel](#newschannel-structure) | newsChannel |


### Example

```
52 00 00 00 21 01 24 00 00 00 01 80 00 00 02 00 00 00 02 00 00 00 00 00 00 00 00 00 40 00 09 00 00 00 00 00 00 00 01 00 00 00 00 00 00 00 0C 00 44 65 73 63 72 69 70 74 69 6F 6E 00 05 00 4E 61 6D 65 00 08 00 55 62 69 4E 65 77 73 00 06 00 65 6E 2D 55 53 00 00
```

# Types

## NewsChannel ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
Extends standard [Gathering](https://github.com/kinnay/NintendoClients/wiki/Match-Making-Types#gathering-structure) class.

| Type | Name |
|--|--|
| [Gathering](https://github.com/kinnay/NintendoClients/wiki/Match-Making-Types#gathering-structure) | gathering |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | name |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | class |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | locale |
| Bool | bSubscribable |
