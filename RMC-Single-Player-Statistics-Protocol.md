A custom Hermes RMC service for game stats submission in singleplayer mode.

The definitions come from MacOS version of the game.

| Method ID | Method Name |
|-----------|-------------|
| 1 | [WritePlayerStats](#1-writeplayerstats) |

# (1) WritePlayerStats

## Request

| Type | Name |
|------|------|
| Uint32 | boardId |
| Uint32 | pid |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[Statistic](#statistic-structure)> | playerStats |


## Response

This method does not return anything.

# Types

## Statistic ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Int8 | propertyId |
| Int32 | valueInt |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | valueString |
| Float | valueFloat |
| Int8 | typeValue |
| Int8 | writePolicy |
