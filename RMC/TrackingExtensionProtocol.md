A custom protocol with unclear purpose, used in the player's session as opposed to the standard [tracking service](https://github.com/kinnay/NintendoClients/wiki/Tracking-Protocol-3).

| Method ID | Method Name |
|-----------|-------------|
| 1 | [IsTrackingSessionActive](#1-istrackingsessionactive) |

# (1) IsTrackingSessionActive

Name assumed based on packet structure and real data inspection.

## Request

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | trackingSesId |

Example value: `3039216`.

## Response

| Type | Name |
|------|------|
| Bool | active |