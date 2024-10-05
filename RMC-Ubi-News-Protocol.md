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

# Types

## NewsChannel ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
Extends standard [Gathering](https://github.com/kinnay/NintendoClients/wiki/Match-Making-Types#gathering-structure) class.

| Type | Name |
|--|--|
| [Gathering](https://github.com/kinnay/NintendoClients/wiki/Match-Making-Types#gathering-structure) | gathering |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | unkString1 |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | unkString2 |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | unkString3 |
| Bool | bSubscribable |
