A custom Hermes RMC service for game saves and remote assassin missions/contracts management in singleplayer mode.

The definitions come from MacOS version of the game.

| Method ID | Method Name |
|-----------|-------------|
| 1 | [RegisterSaveGame](#1-registersavegame) |
| 2 | [GetACPLAssassins](#2-getacplassassins) |
| 3 | [GetACPLCash](#3-getacplcash) |
| 4 | [GetACPLCollections](#4-getacplcollections) |
| 5 | [GetACPLContracts](#5-getacplcontracts) |
| 6 | [GetACPLLandmarks](#6-getacpllandmarks) |
| 7 | [UpdateAssassins](#7-updateassassins) |
| 8 | [UpdateContracts](#8-updatecontracts) |
| 9 | [UpdateSaveGame](#9-updatesavegame) |

# (1) RegisterSaveGame

## Request

| Type | Name |
|------|------|
| Int8 | displayIndex |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | label |
| Uint32 | lastsavetime |


## Response

| Type | Name |
|------|------|
| Uint64 | sgid |

# (2) GetACPLAssassins

## Request

| Type | Name |
|------|------|
| Uint64 | sgid |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[ACPLAssassinType](#acplassassintype-structure)> | assassins |

# (3) GetACPLCash

## Request

This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| Uint32 | cash |

# (4) GetACPLCollections

## Request

This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| Uint32 | collections |

# (5) GetACPLContracts

## Request

| Type | Name |
|------|------|
| Uint64 | sgid |

## Response

| Type | Name |
|------|------|
| Uint32 | contracts |

# (6) GetACPLLandmarks

## Request

This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| Uint32 | landmarks |

# (7) UpdateAssassins

## Request

| Type | Name |
|------|------|
| Uint64 | sgid |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[AssassinType](#assassintype-structure)> | assassins |

## Response

This method does not return anything.

# (8) UpdateContracts

## Request

| Type | Name |
|------|------|
| Uint64 | sgid |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[ContractType](#contracttype-structure)> | contracts |

## Response

This method does not return anything.

# (9) UpdateSaveGame

## Request

| Type | Name |
|------|------|
| Uint64 | sgid |
| Uint32 | lastsavetime |

## Response

This method does not return anything.

# Types

## ACPLAssassinType ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | id |
| Uint32 | xp |

## AssassinType ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | armor |
| Uint32 | id |
| Uint32 | gear |
| Uint32 | gender |
| Uint32 | icon |
| Uint32 | level |
| Uint32 | name |
| Uint32 | weapon |
| Uint32 | xp |

## ContractType ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | contract_unlock |
| Uint32 | contract_success |
