A custom Hermes RMC service for social activity management. No trace of standard usage in ACB or Ghost Recon Future Soldier.

| Method ID | Method Name |
|-----------|-------------|
| 1 | [PostTwitterMessage](#1-posttwittermessage) |
| 2 | [PostFBMessage](#2-postfbmessage) |
| 3 | [RevokeFBAuthorization](#3-revokefbauthorization) |
| 4 | [RevokeTwitterAuthorization](#4-revoketwitterauthorization) |
| 5 | [HasFBAuthorization](#5-hasfbauthorization) |
| 6 | [HasTwitterAuthorization](#6-hastwitterauthorization) |

# (1) PostTwitterMessage

## Request

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | message |

## Response

This method does not return anything.

# (2) PostFBMessage

## Request

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | unkStr1 |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | unkStr2 |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | unkStr3 |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | unkStr4 |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | unkStr5 |

## Response

This method does not return anything.

# (3) RevokeFBAuthorization

## Request

This method does not take any parameters.

## Response

This method does not return anything.

# (4) RevokeTwitterAuthorization

## Request

This method does not take any parameters.

## Response

This method does not return anything.

# (5) HasFBAuthorization

## Request

This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| Bool | %retval% |

# (6) HasTwitterAuthorization

## Request

This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| Bool | %retval% |
