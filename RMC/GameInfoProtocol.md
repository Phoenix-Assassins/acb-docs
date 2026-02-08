A custom Hermes RMC service for session membership management.

| Method ID | Method Name |
|-----------|-------------|
| 1 | [SetSessionMember](#1-setsessionmember) |
| 2 | [RemoveSessionMember](#2-removesessionmember) |
| 3 | [GetSessionMembersCount](#3-getsessionmemberscount) |
| 4 | [GetParticipantsFromParameter](#4-getparticipantsfromparameter) |
| 5 | [GetFileListOnGameStorage](#5-getfilelistongamestorage) |

# (1) SetSessionMember

## Request

| Type | Name |
|------|------|
| [SessionMember](#sessionmember-structure) | sesMember |

## Response

This method does not return anything.

# (2) RemoveSessionMember

## Request

This method does not take any parameters.

## Response

This method does not return anything.

# (3) GetSessionMembersCount

## Request

| Type | Name |
|------|------|
| [SessionMember](#sessionmember-structure) | sesMember |

## Response

| Type | Name |
|------|------|
| Uint32 | sesMemberCount |

# (4) GetParticipantsFromParameter

## Request

| Type | Name |
|------|------|
| Uint32 | param |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[Participant](#participant-structure)> | participants |

# (5) GetFileListOnGameStorage

## Request
The game requests data on game settings originally stored in `.cxb` files, e.g. `gamesettings_c1380_d873_s6285.cxb` (hardcoded in MP binary). Numbers of elements are hardcoded too - respectively 0 and 50.

| Type | Name |
|------|------|
| Uint32 | minNbElements |
| Uint32 | maxNbElements |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | fileName |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[File](#file-structure)> |  files |

# Types

## File ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | fileName |
| Uint32 | fileSize |

Name `fileSize` was assumed, example value was `58 484`.

## Participant ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| Uint32 | unkUint2 |

## SessionMember ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| Uint32 | unkUint2 |
| Uint32 | unkUint3 |
| Uint32 | unkUint4 |
| Uint32 | unkUint5 |
| Uint32 | unkUint6 |
| Uint32 | unkUint7 |
| Uint32 | unkUint8 |
| Uint32 | unkUint9 |