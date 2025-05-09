A Ubi OSDK service for locale management and configuration.

The definitions come from MacOS version of the game.

| Method ID | Method Name |
|-----------|-------------|
| 1 | [CreateLocalization](#1-createlocalization) |
| 2 | [UpdateLocalization](#2-updatelocalization) |
| 3 | [DeleteLocalization](#3-deletelocalization) |
| 4 | [GetNumberOfLocalizationContext](#4-getnumberoflocalizationcontext) |
| 5 | [GetLocalizationContexts](#5-getlocalizationcontexts) |
| 6 | [GetLocalizationStrings](#6-getlocalizationstrings) |
| 7 | [CreatePlaceholderString](#7-createplaceholderstring) |
| 8 | [ParsePlaceholderString](#8-parseplaceholderstring) |

# (1) CreateLocalization

## Request

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | localizationContext |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[LocalizationString](#localizationstring-structure)> | localizedStrings |

## Response

| Type | Name |
|------|------|
| Uint32 | localizationID |

# (2) UpdateLocalization

## Request

| Type | Name |
|------|------|
| Uint32 | localizationID |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[LocalizationString](#localizationstring-structure)> | localizedStrings |

## Response

This method does not return anything.

# (3) DeleteLocalization

## Request

| Type | Name |
|------|------|
| Uint32 | localizationID |

## Response

This method does not return anything.

# (4) GetNumberOfLocalizationContext

## Request

This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| Uint32 | numberOfLocalizationContext |

# (5) GetLocalizationContexts

## Request

| Type | Name |
|------|------|
| [ResultRange](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#resultrange-structure) | range |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[LocalizationContext](#localizationcontext-structure)> | localizationContexts |

# (6) GetLocalizationStrings

## Request

| Type | Name |
|------|------|
| Uint32 | localizationID |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[LocalizationString](#localizationstring-structure)> | localizedStrings |

# (7) CreatePlaceholderString

## Request

| Type | Name |
|------|------|
| Uint32 | localizationID |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[LocalizationPlaceholderItem](#localizationplaceholderitem-structure)> | localizationPlaceholderItems |

## Response

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | placeholderString |

# (8) ParsePlaceholderString

## Request

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | placeholderString |

## Response

| Type | Name |
|------|------|
| Uint32 | localizationID |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[LocalizationPlaceholderItem](#localizationplaceholderitem-structure)> | localizationPlaceholderItems |

# Types

## LocalizationString ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_localeCode |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_localizedString |

## LocalizationContext ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | m_ID |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_context |


## LocalizationPlaceholderItem ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_key |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_value |
