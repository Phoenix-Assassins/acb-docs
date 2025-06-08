A custom Hermes RMC service for clan services. This service is likely not used by ACB. The methods present in the game's binary were compare-reversed with Ghost Recon Future Soldier and are listed here for reference.

Note that there were changes in this service between the two games and payloads an/or method names may differ for the same IDs.

| Method ID | Method Name |
|-----------|-------------|
| 1 | [CreateClan](#1-createclan) |
| 2 | [UpdateClan](#2-updateclan) |
| 3 | [GetClanInfo](#3-getclaninfo) |
| 4 | [DeleteClan](#4-deleteclan) |
| 5 | [InviteToClan](#5-invitetoclan) |
| 6 | [InviteToClanWithName](#6-invitetoclanwithname) |
| 7 | [RemoveInvite](#7-removeinvite) |
| 8 | [JoinClan](#8-joinclan) |
| 9 | [LeaveClan](#9-leaveclan) |
| 10 | [GetInviteInfo](#10-getinviteinfo) |
| 11 | [ChangeRole](#11-changerole) |
| 12 | [ChangeRolePrivilege](#12-changeroleprivilege) |
| 13 | [GetCurUserClan](#13-getcurruserclan) |
| 14 | [GetClanMembers](#14-getclanmembers) |
| 15 | [SetRoom](#15-setroom) |
| 16 | [GetRooms](#16-getrooms) |
| 17 | [JoinRoom](#17-joinroom) |
| 18 | [SetClanRoomState](#18-setclanroomstate) |
| 19 | [GetSortedClanIds](#19-getsortedclanids) |
| 20 | [GetSortedClans](#20-getsortedclans) |
| 21 | [SetClanProperty](#21-setclanproperty) |
| 22 | [RemoveEvent](#22-removeevent) |
| 23 | [SetEvent](#23-setevent) |
| 24 | [GetEvents](#24-getevents) |
| 25 | [ChangeEventType](#25-changeeventtype) |
| 26 | [SendClanMessage](#26-sendclanmessage) |

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

## Response

| Type | Name |
|------|------|
| Uint32 | unkUint |

# (3) GetClanInfo

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

This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| Uint32 | unkUint |

# (5) InviteToClan

## Request

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| Uint32 | unkUint2 |

## Response

| Type | Name |
|------|------|
| Uint32 | unkUint |

# (6) InviteToClanWithName

## Request

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | name |
| Uint32 | clanId |

## Response

| Type | Name |
|------|------|
| Uint32 | unkUint |

# (7) RemoveInvite

## Request

| Type | Name |
|------|------|
| Uint32 | unkInt1 |
| Uint32 | unkInt2 |

## Response

| Type | Name |
|------|------|
| Uint32 | unkUint |

# (8) JoinClan

## Request

| Type | Name |
|------|------|
| Uint32 | clanId |

## Response

| Type | Name |
|------|------|
| Uint32 | unkUint |

# (9) LeaveClan

## Request

| Type | Name |
|------|------|
| Uint32 | unkUint |

## Response

| Type | Name |
|------|------|
| Uint32 | unkUint |

# (10) GetInviteInfo

## Request

| Type | Name |
|------|------|
| Uint32 | unkInt |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[ClanInvite](#claninvite-structure)> | clanInvites |

# (11) ChangeRole

## Request

| Type | Name |
|------|------|
| Uint32 | unkInt1 |
| Uint32 | unkInt2 |

## Response

| Type | Name |
|------|------|
| Uint32 | unkInt |

# (12) ChangeRolePrivilege

## Request

| Type | Name |
|------|------|
| Uint32 | unkInt1 |
| Uint32 | unkInt2 |

## Response

| Type | Name |
|------|------|
| Uint32 | unkInt |

# (13) GetCurUserClan

## Request

This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| Uint32 | clanId |

# (14) GetClanMembers

## Request

| Type | Name |
|------|------|
| Uint32 | unkUint |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[ClanMember](#clanmember-structure)> | clanMembers |

# (15) SetRoom

## Request

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string)| unkString |
| Uint8 | unkByte |
| Bool | unkBool |

## Response

| Type | Name |
|------|------|
| Uint32 | unkUint |

# (16) GetRooms

## Request

| Type | Name |
|------|------|
| Uint8 | unkByte1 |
| Uint8 | unkByte2 |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[ClanRoom](#clanroom-structure)> | clanRooms |

# (17) JoinRoom

## Request

| Type | Name |
|------|------|
| Uint8 | unkByte |

## Response

This method does not return anything.

# (18) SetRoomState

## Request

| Type | Name |
|------|------|
| Uint8 | unkByte1 |
| Uint8 | unkByte2 |

## Response

This method does not return anything.

# (19) GetSortedClanIds

## Request

| Type | Name |
|------|------|
| Uint8 | unkByte |
| Uint32 | unkUint1 |
| Uint32 | unkUint2 |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)\<Uint32> | clanIds |
| Uint32 | unkUint |

# (20) GetSortedClans

## Request

| Type | Name |
|------|------|
| Uint8 | unkByte |
| Uint32 | unkUint1 |
| Uint32 | unkUint2 |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[Clan](#clan-structure)> | clans |
| Uint32 | unkUint |

# (21) SetClanProp

## Request

| Type | Name |
|------|------|
| Uint32 | clanId |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[ClanProperty](#clanproperty-structure)> | clanProps |

## Response

This method does not return anything.

# (22) RemoveEvent

## Request

| Type | Name |
|------|------|
| Uint32 | unkInt |

## Response

| Type | Name |
|------|------|
| Uint32 | unkUint |

# (23) SetEvent

## Request

| [ClanEvent](#clanevent-structure) | clanEvent |

## Response

| Type | Name |
|------|------|
| Uint32 | unkUint |

# (24) GetEvents

## Request

| Type | Name |
|------|------|
| Uint32 | unkUint |
| Uint8 | unkByte |
| [DateTime](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#datetime) | date1 |
| [DateTime](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#datetime) | date2 |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[ClanEvent](#clanevent-structure)> | clanEvents |

# (25) ChangeEventType

## Request

| Type | Name |
|------|------|
| Uint32 | unkInt |
| Uint8 | unkByte |

## Response

| Type | Name |
|------|------|
| Uint32 | unkUint |

# (26) SendClanMessage

## Request

| Type | Name |
|------|------|
| Uint8 | unkByte1 |
| Uint32 | unkInt1 |
| Uint32 | unkInt2 |
| Uint8 | unkByte2 |
| Uint8 | unkByte3 |
| Uint32 | unkInt3 |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | message |

## Response

This method does not return anything.

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

## ClanProperty ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | unkUint |
| Uint8 | unkByte1 |
| Uint8 | unkByte2 |

## ClanEvent ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| Uint32 | unkUint2 |
| Uint32 | unkUint3 |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string)| unkString |
| Uint8 | unkByte |
| [DateTime](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#datetime) | date1 |
| [DateTime](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#datetime) | date2 |

## ClanInvite ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| Uint32 | unkUint2 |
| Uint32 | unkUint3 |
| [DateTime](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#datetime) | date |

## ClanMember ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| Uint8 | unkByte1 |
| [DateTime](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#datetime) | date |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string)| unkString |
| Uint8 | unkByte2 |

## ClanRoom ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint8 | unkByte1 |
| Uint8 | unkByte2 |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string)| unkString |
