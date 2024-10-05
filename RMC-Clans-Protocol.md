A custom Hermes RMC service for clan services. This service is likely not used by ACB. The methods present in the game's binary were compare-reversed with Ghost Recon Future Soldier and are listed here for reference.

Note that there were changes in this service between the two games and payloads an/or method names may differ for the same IDs.

| Method ID | Method Name |
|-----------|-------------|
| 1 | [CreateClan](#1-createclan) |
| 2 | [UpdateClan](#2-updateclan) |
| 3 | [GetClanList](#3-getclanlist) |
| 4 | [DeleteClan](#4-deleteclan) |
| 5 | [InviteToClan](#5-invitetoclan) |
| 6 | [InviteToClanWithName](#6-invitetoclanwithname) |
| 7 | [RemoveClanInvite](#7-removeclaninvite) |
| 8 | [JoinClan](#8-joinclan) |
| 9 | [LeaveClan](#9-leaveclan) |
| 10 | [GetClanInvites](#10-getclaninvites) |
| 11 | [ChangeClanRole](#11-changeclanrole) |
| 12 | [ChangeClanRolePriv](#12-changeclanrolepriv) |
| 13 | [GetCurUserClan](#13-getcurruserclan) |
| 14 | [GetClanMembers](#14-getclanmembers) |
| 15 | [SetClanRoom](#15-setclanroom) |
| 16 | [DownloadClanRoomInfo](#16-downloadclanroominfo) |
| 17 | [JoinClanRoom](#17-joinclanroom) |
| 18 | [SetClanRoomState](#18-setclanroomstate) |
| 19 | [GetClanLeaderboard](#19-getclanleaderboard) |
| 20 | [?]() |
| 21 | [SetClanProperty](#21-setclanproperty) |
| 22 | [RemoveClanEvent](#22-removeclanevent) |
| 23 | [SetClanEvent](#23-setclanevent) |
| 24 | [GetClanEvents](#24-getclanevents) |
| 25 | [ChangeEventType](#25-changeeventtype) |
| 26 | [SendClanMessage??]() |

# (1) CreateClan

## Request

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | unkString1 |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | unkString2 |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | unkString3 |

## Response

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| Uint32 | unkUint2 |

# (2) UpdateClan

## Request
This is the payload present in ACB - GRFS has `Uint8 unkByte` instead of `unkString3`.

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | unkString1 |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | unkString2 |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | unkString3 |

## Response

| Type | Name |
|------|------|
| Uint32 | unkUint |

# (3) GetClanList

## Request

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)\<Uint32\> | clanIds |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[Clan](#clan-structure)> | clans |

# (4) DeleteClan

## Request


## Response


# (5) InviteToClan

## Request


## Response


# (6) InviteToClanWithName

## Request


## Response


# (7) RemoveClanInvite

## Request


## Response


# (8) JoinClan

## Request


## Response


# (9) LeaveClan

## Request


## Response


# (10) GetClanInvites

## Request


## Response


# (11) ChangeClanRole

## Request


## Response


# (12) ChangeClanRolePriv

## Request


## Response


# (13) GetCurUserClan

## Request


## Response

# (14) GetClanMembers

## Request


## Response


# (15) SetClanRoom

## Request


## Response


# (16) DownloadClanRoomInfo

## Request


## Response


# (17) JoinClanRoom

## Request


## Response


# (18) SetClanRoomState

## Request


## Response


# (19) GetClanLeaderboard

## Request


## Response


# (20) ?

## Request


## Response


# (21) SetClanProperty

## Request


## Response


# (22) RemoveClanEvent

## Request


## Response


# (23) SetClanEvent

## Request


## Response


# (24) GetClanEvents

## Request


## Response


# (25) ChangeEventType

## Request


## Response


# (26) SendClanMessage??

## Request


## Response

# Types

## Clan ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

This is ACB version of Clan structure.

| Type | Name |
|------|------|
| Uint32 | unkUint |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string)| unkString1 |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string)| unkString2 |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string)| unkString3 |
| Uint8 | unkByte |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)\<Uint8\>| unkUshorts |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)\<Uint32\> | ukUints |
