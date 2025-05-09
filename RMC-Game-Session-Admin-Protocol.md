A Ubi OSDK service for game session management and configuration.

The definitions come from MacOS version of the game.

| Method ID | Method Name |
|-----------|-------------|
| 1 | [GetTableStatuses](#1-gettablestatuses) |
| 2 | [ForceCustomTableSync](#2-forcecustomtablesync) |
| 3 | [CleanupOnBootSessions](#3-cleanuponbootsessions) |
| 4 | [CleanupOnBootURLs](#4-cleanuponbooturls) |
| 5 | [GetURLs](#5-geturls) |
| 6 | [UpdateURLsDID](#6-updateurlsdid) |
| 7 | [SetThrottlingProbability](#7-setthrottlingprobability) |
| 8 | [SetThrottlingDelay](#8-setthrottlingdelay) |
| 9 | [GetSession](#9-getsession) |

# (1) GetTableStatuses

## Request

This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[GameSessionTableStatus](#gamesessiontablestatus-structure)> | gameSessionTableStatuses |

# (2) ForceCustomTableSync

## Request

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[GameSessionTableDetail](#gamesessiontabledetail-structure)> | gameSessionTableDetails |

## Response

This method does not return anything.

# (3) CleanupOnBootSessions

## Request

This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| Uint32 | nbOfAffectedRows |

# (4) CleanupOnBootURLs

## Request

This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| Uint32 | nbOfAffectedRows |

# (5) GetURLs

## Request

| Type | Name |
|------|------|
| Uint32 | pid |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[StationURL](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#stationurl)> | urls |

# (6) UpdateURLsDID

## Request

| Type | Name |
|------|------|
| Uint32 | pid |
| Uint32 | did |

## Response

This method does not return anything.

# (7) SetThrottlingProbability

## Request

| Type | Name |
|------|------|
| Uint32 | typeID |
| Uint32 | throttlingPercentage |

## Response

This method does not return anything.

# (8) SetThrottlingDelay

## Request

| Type | Name |
|------|------|
| Uint32 | typeID |
| Uint32 | throttlingDelaySeconds |

## Response

This method does not return anything.

# (9) GetSession

## Request

| Type | Name |
|------|------|
| [GameSessionKey](https://github.com/kinnay/NintendoClients/wiki/Game-Session-Protocol#gamesessionkey-structure) | gameSessionKey |

## Response

| Type | Name |
|------|------|
| [GameSessionSearchResult](https://github.com/kinnay/NintendoClients/wiki/Game-Session-Protocol#gamesessionsearchresult-structure) | searchResult |

# Types

## GameSessionTableStatus ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_tableName |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_engine |
| [DateTime](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#datetime) | m_creationTime |

## GameSessionTableDetail ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_tableName |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_generatorVersion |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_xmlHash |
