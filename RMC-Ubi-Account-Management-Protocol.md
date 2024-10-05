OSDK account management service likely implemented by Ubisoft after taking over Quazal Technologies.

| Method ID | Method Name |
|---|---|
| 1 | [CreateAccount](#1-createaccount) |
| 2 | [UpdateAccount](#2-updateaccount) |
| 3 | [GetAccount](#3-getaccount) |
| 4 | [LinkAccount](#4-linkaccount) |
| 5 | [GetTOS](#5-gettos) |
| 6 | [ValidateUsername](#6-validateusername) |
| 7 | [ValidatePassword](#7-validatepassword) |
| 8 | [ValidateEmail](#8-validateemail) |
| 9 | [GetCountryList](#9-getcountrylist) |
| 10 | [ForgetPassword](#10-forgetpassword) |

# (1) CreateAccount
## Request

| Type | Name |
|--|--|
| [UbiAccount](#ubiaccount-structure) | ubiAccount |

## Response

| Type | Name |
|--|--|
| [UbiAccount](#ubiaccount-structure) | ubiAccount |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[ValidationFailureReason](#validationfailurereason-structure)> | failedReasons |

# (2) UpdateAccount
## Request

| Type | Name |
|--|--|
| [UbiAccount](#ubiaccount-structure) | ubiAccount |

## Response

| Type | Name |
|--|--|
| [UbiAccount](#ubiaccount-structure) | ubiAccount |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[ValidationFailureReason](#validationfailurereason-structure)> | failedReasons |

# (3) GetAccount
## Request

This method does not take any parameters.

## Response

| Type | Name |
|--|--|
| [UbiAccount](#ubiaccount-structure) | ubiAccount |
| Bool | exists |

# (4) LinkAccount
## Request

| Type | Name |
|--|--|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | ubiAccountUsername |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | ubiAccountPassword |

## Response

| Type | Name |
|--|--|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | ubiAccountUsername |

# (5) GetTOS
## Request

| Type | Name |
|--|--|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | countryCode |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | languageCode |
| Bool | htmlVersion |

## Response

| Type | Name |
|--|--|
| [TOS](#tos-structure) | tos |

# (6) ValidateUsername
## Request

| Type | Name |
|--|--|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | username |

## Response

| Type | Name |
|--|--|
| [UsernameValidation](#usernamevalidation-structure) | usernameValidation |

# (7) ValidatePassword
## Request

| Type | Name |
|--|--|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | password |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | username |

## Response

| Type | Name |
|--|--|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[ValidationFailureReason](#validationfailurereason-structure)> | failedReasons |

# (8) ValidateEmail
## Request

| Type | Name |
|--|--|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | email |

## Response

| Type | Name |
|--|--|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[ValidationFailureReason](#validationfailurereason-structure)> | failedReasons |


# (9) GetCountryList
## Request

| Type | Name |
|--|--|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | languageCode |

## Response

| Type | Name |
|--|--|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[Country](#country-structure)> | countries |

# (10) ForgetPassword
## Request

| Type | Name |
|--|--|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | usernameOrEmail |

## Response

This method does not return anything.

# Types

## Country ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|--|--|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_code |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_name |

## ExternalAccount ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|--|--|
| Uint32 | m_accountType |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_id |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_username |

## UbiAccountStatus ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|--|--|
| Uint32 | m_basicStatus |
| Bool | m_missingRequiredInformations |
| Bool | m_recoveringPassword |
| Bool | m_pendingDeactivation |

## UbiAccount ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|--|--|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_ubiAccountId |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_username |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_password |
| [UbiAccountStatus](#ubiaccountstatus-structure) | m_status |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_email |
| [DateTime](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#datetime) | m_dateOfBirth |
| Uint32  | m_gender |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_countryCode |
| Bool | m_optIn |
| Bool | m_thirdPartyOptIn |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_firstName |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_lastName |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_preferredLanguage |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[ExternalAccount](#externalaccount-structure)> | m_externalAccounts |

## TOS ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|--|--|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_localeCode |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_content |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_storingInfoQuestion |

## ValidationFailureReason ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|--|--|
| Uint32   | m_validationId |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_description |

## UsernameValidation ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|--|--|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[String]()> | m_suggestions |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[ValidationFailureReason](#validationfailurereason-structure)> | m_reasons |
