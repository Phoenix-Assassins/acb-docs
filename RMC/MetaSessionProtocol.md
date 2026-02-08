A custom Hermes RMC service for backend metasessions.

| Method ID | Method Name |
|-----------|-------------|
| 1 | [SendConnectionInformation](#1-sendconnectioninformation) |
| 2 | [RetrieveSubSessionInformation](#2-retrievesubsessioninformation) |
| 3 | [SendSessionKey](#3-sendsessionkey) |
| 4 | [GetSessionKey](#4-getsessionkey)  |
| 5 | [JoinMetaSession](#5-joinmetasession) |
| 6 | [JoinMetasessionWithId](#6-joinmetasessionwithid) |
| 7 | [ChooseSubSession](#7-choosesubsession) |
| 8 | [SearchMetasession](#8-searchmetasession) |
| 9 | [ValidateConnection](#9-validateconnection) |
| 10 | [ValidateConnectionInfo](#10-validateconnectioninfo) |
| 11 | [LeaveMetaSession](#11-leavemetasession) |
| 12 | [UpdateScore](#12-updatescore) |
| 13 | [GetRanking](#13-getranking) |
| 14 | [UpdateNewHost](#14-updatenewhost) |
| 15 | [UpdateNewHostWithArguments](#15-updatenewhostwitharguments) |
| 16 | [IsPresentInMetasessionPCPlatform](#16-ispresentinmetasessionpcplatform) |
| 17 | [IsPresentInMetasessionPS3Platform](#17-ispresentinmetasessionps3platform) |
| 18 | [IsPresentInMetasessionXboxPlatform](#18-ispresentinmetasessionxboxplatform) |

# (1) SendConnectionInformation

## Request

| Type | Name |
|------|------|
| [qBuffer](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#qbuffer) | buffer |

## Response

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| Uint32 | unkUint2 |

# (2) RetrieveSubSessionInformation

## Request

This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| [qBuffer](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#qbuffer) | buffer |
| Uint32 | unkUint |

# (3) SendSessionKey

## Request

| Type | Name |
|------|------|
| [qBuffer](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#qbuffer) | sesKey |

## Response

| Type | Name |
|------|------|
| Uint32 | unkUint |

# (4) GetSessionKey

## Request

This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| [qBuffer](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#qbuffer) | buffer |
| Uint32 | unkUint |

# (5) JoinMetaSession

## Request

| Type | Name |
|------|------|
| [MetaSessionInfo](#metasessioninfo-structure) | metaSesInfo |
| Uint32 | unkUint |

## Response

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| Uint32 | unkUint2 |

# (6) JoinMetasessionWithId

## Request

| Type | Name |
|------|------|
| Uint32 | metaSesId |

## Response

| Type | Name |
|------|------|
| Uint32 | unkUint |

# (7) ChooseSubSession

## Request

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string)> | unkStrings |

## Response

| Type | Name |
|------|------|
| [SubSession](#subsession-structure) | subSession |
| Uint32 | unkUint1 |
| Uint32 | unkUint2 |

# (8) SearchMetasession

## Request

This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[MetaSession](#metasession-structure)> | metaSessions |

# (9) ValidateConnection

## Request


| Type | Name |
|------|------|
| Bool | unkBool |

## Response

This method does not return anything.

# (10) ValidateConnectionInfo

## Request

| Type | Name |
|------|------|
| Bool | unkBool |
| [qBuffer](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#qbuffer) | connInfo |

## Response

This method does not return anything.

# (11) LeaveMetaSession

## Request

This method does not take any parameters.

## Response

This method does not return anything.

# (12) UpdateScore

## Request

| Type | Name |
|------|------|
| [List]()<[MetaSessionScore]()> | metaSesScores |

## Response

This method does not return anything.

# (13) GetRanking

## Request

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| Uint32 | unkUint2 |
| Uint32 | unkUint3 |

## Response

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[RankingMetaSessionPlayer](#rankingmetasessionplayer -structure)> | players |
| Bool | unkBool |
| Uint32 | unkUint2 |

# (14) UpdateNewHost

## Request

This method does not take any parameters.

## Response

This method does not return anything.

# (15) UpdateNewHostWithArguments

## Request

| Type | Name |
|------|------|
| [qBuffer](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#qbuffer) | buffer |

## Response

This method does not return anything.

# (16) IsPresentInMetasessionPCPlatform

## Request

| Type | Name |
|------|------|
| Uint32 | pid |

## Response

| Type | Name |
|------|------|
| Bool | bPresent |
| Uint32 | unkUint |
| [MetaSessionInfo](#metasessioninfo-structure) | metaSesInfo |

# (17) IsPresentInMetasessionPS3Platform

## Request

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | unkString |

## Response

| Type | Name |
|------|------|
| Bool | bPresent|
| Uint32 | unkUint |
| [MetaSessionInfo](#metasessioninfo-structure) | metaSesInfo |

# (18) IsPresentInMetasessionXboxPlatform

## Request

| Type | Name |
|------|------|
| Uint64 | metaSesId |

## Response

| Type | Name |
|------|------|
| Bool | bPresent|
| Uint32 | unkUint |
| [MetaSessionInfo](#metasessioninfo-structure) | metaSesInfo |

# Types

## MetaSessionInfo ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

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
| Uint32 | unkUint10 |


## SubSession ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| Uint32 | unkUint2 |
| Bool | unkBool1 |
| Bool | unkBool2 |


## MetaSession ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| Uint32 | unkUint2 |
| [MetaSessionInfo](#metasessioninfo-structure) | metaSesInfo |
| Uint32 | unkUint3 |

## MetaSessionScore  ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| Uint32 | policy |
| Uint32 | unkUint2 |

## RankingMetaSessionPlayer ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| Uint32 | unkUint2 |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | unkString |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[MetaSessionScore](#metasessionscore-structure)>| metaSesScores |
