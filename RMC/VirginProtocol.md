Seemingly a dependency on a late version of Scimitar engine, Virgin is attention-attracting name for custom reporting RMC service for basic player information.

| Method ID | Method Name |
|---|---|
| 1 | [SendVirginInformation](#1-sendvirgininformation) |

# (1) SendVirginInformation

## Request

| Type | Name |
|---|---|
| Uint32 | pid |
| Uint64 | sessionID |
| [DateTime](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#datetime) | begin |
| [DateTime](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#datetime) | end |
| Bool | host |
| Bool  | hasQuit |
| Int32 | uniquePlayerMax |
| Int8 | gameMode |
| Int8  | platform |
| Int32  | score |
| Int32  | killNumber |

## Response

This method does not return anything.