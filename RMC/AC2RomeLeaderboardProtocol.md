A custom Hermes RMC service for Rome restoration progress stats in singleplayer mode.

The definitions come from MacOS version of the game.

| Method ID | Method Name |
|-----------|-------------|
| 1 | [SubmitStats](#1-submitstats) |
| 2 | [GetFriendScores](#2-getfriendscores) |
| 3 | [GetPlayerRanks](#3-getplayerranks) |
| 4 | [GetRanksCount](#4-getrankscount) |
| 5 | [GetRanks](#5-GetRanks) |
| 6 | [GetRanksNearPlayer](#6-getranksnearplayer) |

# (1) SubmitStats

## Request

| Type | Name |
|------|------|
| Uint32 | missionType |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)\<Uint32> | friendIDs |
| Uint32 | timeInMilliseconds |

## Response

This method does not return anything.

# (2) GetFriendScores

## Request

| Type | Name |
|------|------|
| Uint32 | missionType |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)\<Uint32> | friendIDs |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[StatboardEntry](#statboardentry-structure)> | statboardEntries |

# (3) GetPlayerRanks

## Request

| Type | Name |
|------|------|
| Uint32 | missionType |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)\<Uint32> | playerIDs |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[LeaderboardEntry](#leaderboardentry-structure)> | leaderboardEntries |

# (4) GetRanksCount

## Request

| Type | Name |
|------|------|
| Uint32 | missionType |

## Response

| Type | Name |
|------|------|
| Uint32 | count |

# (5) GetRanks

## Request

| Type | Name |
|------|------|
| Uint32 | missionType |
| [ResultRange](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#resultrange-structure) | resultRange |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[LeaderboardEntry](#leaderboardentry-structure)> | leaderboardEntries |

# (6) GetRanksNearPlayer

## Request

| Type | Name |
|------|------|
| Uint32 | missionType |
| Uint32 | playerID |
| Uint32 | count |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[LeaderboardEntry](#leaderboardentry-structure)> | leaderboardEntries |

# Types

## StatboardEntry ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | m_playerID |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_playerName |
| Uint32 | m_score |

## LeaderboardEntry ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | m_rank |
| [StatboardEntry](#statboardentry-structure) | m_statboardEntry |
