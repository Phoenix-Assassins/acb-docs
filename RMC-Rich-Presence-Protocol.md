A custom Hermes RMC service for player rich presence inside the game.

| Method ID | Method Name |
|-----------|-------------|
| 1 | SetPresence |
| 2 | GetPresence |

# (1) SetPresence

## Request

| Type | Name |
|------|------|
| Uint32 | pid |
| [qBuffer](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#qbuffer) | buffer |

## Response

This method does not return anything.

# (2) GetPresence

## Request

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)\<Uint32> | playerIds |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[PresenceElement](#presenceelement-structure)> | presenceElements |


# Types

## PresenceElement ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| Bool | unkBool |
| Uint32 | unkUint2 |
| [qBuffer](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#qbuffer) | buffer |
