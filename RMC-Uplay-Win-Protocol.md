Ubisoft's service for Uplay integration, used for actions, rewards, purchases and in-game currency.
The service schema was found in Ghost Recon Online's binary, it misses 2 methods present in ACB.

| Method ID | Method Name |
|-----------|-------------|
| 1 | [GetActions](#1-getactions) |
| 2 | [GetActionsCompleted](#2-getactionscompleted) |
| 3 | [GetActionsCount](#3-getactionscount) |
| 4 | [GetActionsCompletedCount](#4-getactionscompletedcount) |
| 5 | [GetRewards](#5-getrewards) |
| 6 | [GetRewardsPurchased](#6-getrewardspurchased) |
| 7 | [UplayWelcome](#7-uplaywelcome) |
| 8 | [SetActionCompleted](#8-setactioncompleted) |
| 9 | [SetActionsCompleted](#9-setactionscompleted) |
| 10 | [Unknown](#10-unknown) |
| 11 | [GetUserToken](#11-getusertoken) |
| 12 | [Unknown](#12-unknown) |
| 13 | [GetVirtualCurrencyUserBalance](#13-getvirtualcurrencyuserbalance) |
| 14 | [GetSectionsByKey](#14-getsectionsbykey) |

# (1) GetActions

## Request

| Type | Name |
|------|------|
| Uint32 | startRowIndex |
| Uint32 | maximumRows |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | sortExpression |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | cultureName |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | platformCode|


## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[UplayAction](#uplayaction)> | actionList |

# (2) GetActionsCompleted

## Request

| Type | Name |
|------|------|
| Uint32 | startRowIndex |
| Uint32 | maximumRows |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | sortExpression |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | cultureName |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | platformCode|


## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[UplayAction](#uplayaction)> | actionList |

# (3) GetActionsCount

## Request

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | platformCode|


## Response

| Type | Name |
|------|------|
| Uint32 | actionsCount |

# (4) GetActionsCompletedCount

## Request

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | platformCode|


## Response

| Type | Name |
|------|------|
| Uint32 | actionsCount |

# (5) GetRewards

## Request

| Type | Name |
|------|------|
| Uint32 | startRowIndex |
| Uint32 | maximumRows |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | sortExpression |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | cultureName |
| ~~[String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string)~~ | ~~platformCode~~* |

*GRO added `platformCode` to the request, it does not exist in ACB.

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[UplayReward](#uplayreward)> | rewardList |

## Data
Available rewards:

| Code | Name | Description | Value | Type | Game code |
|---|---|---|---|---|---|
| ACBREWARD02 | Florentine nobleman outfit | Dress Ezio in the clothes he wore as a Florentine noble. | 20 | Unlockable | ACB |
| ACBREWARD03 | Altaïr's armor | Dress Ezio in Altaïr's armor. | 20 | Unlockable | ACB |
| ACBREWARD04 | Altaïr's robes | Dress Ezio in Altaïr's assassin robes. | 20 | Unlockable | ACB |
| ACBREWARD05 | Weapon pouch upgrade | Increase your firearm's capacity to 10 rounds. | 30 | Unlockable | ACB |
| ACBREWARD06 | Unlock Harlequin | Play as Harlequin. | 40 | Unlockable | ACB |
| ACBREWARD07 | The Da Vinci Disappearance | Help Ezio rescue the kidnapped Leonardo and explore the new possibilities offered by this largest single-player expansion. | 0 | Unlockable | ACB |

# (6) GetRewardsPurchased

## Request

| Type | Name |
|------|------|
| Uint32 | startRowIndex |
| Uint32 | maximumRows |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | sortExpression |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | cultureName |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | platformCode|


## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[UplayReward](#uplayreward)> | rewardList |

# (7) UplayWelcome

## Request

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | cultureName |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | platformCode|


## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[UplayAction](#uplayaction)> | actionList |

# (8) SetActionCompleted

## Request

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | actionCode |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | cultureName |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | platformCode|


## Response

| Type | Name |
|------|------|
| [UplayAction](#uplayaction) | unlockedAction |

# (9) SetActionsCompleted

## Request

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string)> | actionCodeList|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | cultureName |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | platformCode|


## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[UplayAction](#uplayaction)> | actionList |

# (10) Unknown

## Request

Unknown.

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[UplayAction](#uplayaction)> | actionList |

# (11) GetUserToken

## Request

This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | token |

# (12) Unknown

## Request

Unknown.

## Response

| Type | Name |
|------|------|
| Uint16 | unknown |

# (13) GetVirtualCurrencyUserBalance

## Request

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | platformCode |

## Response

| Type | Name |
|------|------|
| Uint32 | virtualCurrencyUserBalance |

# (14) GetSectionsByKey

## Request

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | cultureName |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | sectionKey |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | platformCode |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[UplaySection](#uplaysection)> | sectionList |

# Types

## UplayAction

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_code |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_name |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_description |
| Uint32 | m_value |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_gameCode |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[UplayActionPlatform](#uplayactionplatform)> | m_platforms |

## UplayActionPlatform

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_platformCode |
| Bool | m_completed |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_specificKey |

## UplayReward

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_code |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_name |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_description |
| Uint32| m_value |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_rewardTypeName |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_gameCode |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[UplayRewardPlatform](#uplayrewardplatform)> | m_platforms |

## UplayRewardPlatform

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_platformCode |
| Bool | m_purchased |

## UplaySection

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_key |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_name |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_typeName |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_menuTypeName |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[UplaySectionContent](#uplaysectioncontent)> | m_contentList |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_gameCode |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_platformCode |

## UplaySectionContent

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_key |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_name |
| Uint16 | m_order |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_typeName |
| [UplaySectionContentLocalized](#uplaysectioncontentlocalized) | m_localizedInfo |

## UplaySectionContentLocalized

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_key |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_culture |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_text|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_url |
| Uint32 | m_duration |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_size |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_width |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_height |