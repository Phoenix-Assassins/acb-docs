A custom Hermes RMC service for achievements. No trace of standard usage in ACB or Ghost Recon Future Soldier.

| Method ID | Method Name |
|-----------|-------------|
| 1 | [ReadAchievementDetails](#1-readachievementdetails) |
| 2 | [ReadAchievementSet](#2-readachievementset) |
| 3 | [UnlockAchievements](#3-unlockachievements) |

# (1) ReadAchievementDetails

## Request

| Type | Name |
|------|------|
| Uint32 | unkUint |

## Response

| Type | Name |
|------|------|
| [HermesAchievement](#hermesachievement-structure) | achievement |

# (2) ReadAchievementSet

## Request

This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[HermesAchievement](#hermesachievement-structure)> | achievements |

# (3) UnlockAchievements

## Request

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)\<Uint32\> | achievementIds |

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
