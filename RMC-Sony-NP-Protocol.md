Communication with Sony NP service found inside `UPlayBrowser.exe`.

| Method ID | Method Name |
|-----------|-------------|
| 1 | LookupSceNpIds |
| 2 | LookupPrincipalIds |

# (1) LookupSceNpIds 

## Request

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)\<Uint32> | pids |

## Response

| Type | Name |
|------|------|
| [Map](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#map)<Uint32, [qBuffer](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#qbuffer)> | npids |

# (2) LookupPrincipalIds

## Request

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)\<[qBuffer](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#qbuffer)> | npids |

## Response

| Type | Name |
|------|------|
| [Map](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#map)<[qBuffer](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#qbuffer), Uint32> | pids |
