A custom Hermes RMC service for achievements. No trace of standard usage in ACB or Ghost Recon Future Soldier.

| Method ID | Method Name |
|-----------|-------------|
| 1 | [Unused](#1-unused) |
| 2 | [Unused](#2-unused) |
| 3 | [Unused](#3-unused) |

# (1) Unused

## Request

| Type | Name |
|------|------|
| [HermesAchievement](#hermesachievement-structure) | achievement |


## Response

| Type | Name |
|------|------|
| [HermesAchievement](#hermesachievement-structure) | achievement |

# (2) Unused

## Request

| Type | Name |
|------|------|
| [List]()<[HermesAchievement](#hermesachievement-structure)> | achievements |

## Response

| Type | Name |
|------|------|
| [List]()<[HermesAchievement](#hermesachievement-structure)> | achievements |

# (3) Unused

## Request

| Type | Name |
|------|------|
| | [List]()\<Uint32\> | achievementIds |

## Response

This method does not return anything.

# Types

## HermesAchievement ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | unkString1 |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | unkString2 |
| Bool | unkBool1 |
| Bool | unkBool2 |
| Uint32 | unkUint2 |
| [DateTime](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#datetime) | date |