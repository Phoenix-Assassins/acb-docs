A custom Hermes RMC service for friend game session management.

| Method ID | Method Name |
|-----------|-------------|
| 1 | Unused |
| 2 | Unused |
| 3 | [GetFriendsGameSession](#3-getfriendsgamesession) |

# (1) Unused

## Request

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | unkString |

## Response

Sessions' class might extend the original [`Gathering`](https://github.com/kinnay/NintendoClients/wiki/Match-Making-Types#gathering-structure) type, this method is not used by ACB.

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[Gathering](https://github.com/kinnay/NintendoClients/wiki/Match-Making-Types#gathering-structure)> | sessions |

# (2) Unused

## Request

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string)> | unkStrings |

## Response

Sessions' class might extend the original [`Gathering`](https://github.com/kinnay/NintendoClients/wiki/Match-Making-Types#gathering-structure) type, this method is not used by ACB.

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[Gathering](https://github.com/kinnay/NintendoClients/wiki/Match-Making-Types#gathering-structure)> | sessions |

# (3) GetFriendsGameSession

## Request

| Type | Name |
|------|------|
| Uint32 | unkUint |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string)> | unkStrings |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[FriendGameSessionSearchResult](#friendgamesessionsearchresult-structure)> | frGameSesSearchResults |

# Types

## FriendGameSessionSearchResult ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | unkString |
| Uint32 | unkUint |
| Bool | unkBool1 |
| Bool | unkBool2 |
| [GameSessionSearchResult](https://github.com/kinnay/NintendoClients/wiki/Game-Session-Protocol#gamesessionsearchresult-structure) | gameSesSearchResult |