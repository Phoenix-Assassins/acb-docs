Communication with Xbox LSP service found inside `UPlayBrowser.exe`.


| Method ID | Method Name |
|-----------|-------------|
| 1 | LookupPrincipalIDs |
| 2 | LookupXUIDs |

# (1) LookupPrincipalIDs 

## Request

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)\<Uint64> | xuids |

## Response

| Type | Name |
|------|------|
| [Map](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#map)<Uint64, Uint32> | pids |

# (2) LookupXUIDs 

## Request

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)\<Uint32> | pids |

## Response

| Type | Name |
|------|------|
| [Map](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#map)<Uint32, Uint64> | xuids |
