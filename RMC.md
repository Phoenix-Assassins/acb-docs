Every game built with Quazal uses RMC (Remote Method Calls) protocol to implement the needed backend services. The protocol is used by the authentication server and Rendez-Vous.

# Overview

Quazal's RMC is a backend protocol on top of PRUDP based on RPC-type of services. They were originally called protocols but think of those as microservices, the name is unfortunate so we'll call them services from now on.

Quazal's SDK comes with out-of-the-box services which implemented universal modules of any multiplayer game's networking, such as authentication, matchmaking, friends and many more. The engine module/DLL file which includes them is called OSDK. Quazal also allowed developers to implement their custom services according to their game's needs. Those obviously vary between games and are completely different between publishers - for instance, AC Brotherhood's RMC services are similiar to those of Ghost Recon Phantoms and Ghost Recon Future Soldier (Ubisoft), but are completely different than 25 To Life's (Eidos Interactive).

Every RMC ~~protocol~~ service has its own set of methods (RMC endpoints) which can be called by RMC requests. Each method has an identifier and strictly defined binary data structures for request and response packets.

While for the majority of services transactions are initiated by the game, there are a few services which can or have to be initiated by the server. In the game binary it's defined by the base class of given protocol (that's how they call it there): client-side services inherit from `Quazal::ClientProtocol`, server-side services from `Quazal::ServerProtocol`.

As RMC functions above PRUDP protocol, it is required to set [PRUDP ACK flag](https://github.com/zeroKilo/GROBackendWV/wiki/QPacket-Format#other-prudp-flags) in the response packet or an additional PRUDP packet with ACK flag after a response from the game.

# Packet structure

Below you can see an example of PRUDP packet with RMC packet inside its payload.
```
3F 31 32 9D CD CD CD CD 02 00 00 00 11 00 00 00 8A 04 00 00 00 01 00 00 00 06 00 6D 69 6D 61 6B 00 2D
```

Here's the entire RMC packet extracted:
```
11 00 00 00 8A 04 00 00 00 01 00 00 00 06 00 6D 69 6D 61 6B 00
```

## RMC Header

All the values are big endian-encoded (the least significant byte is on the left).
```
11 00 00 00 8A 04 00 00 00 01 00 00 00
```

Let's break down the header ([see GRO wiki for encoding details](https://github.com/zeroKilo/GROBackendWV/wiki/RMC-Packet-Format#decoding--encoding)):
- `11 00 00 00` - size of the RMC packet (excludes itself and PRUDP checksum), here 17 bytes

- `8A` - protocol (service) ID; for requests it is ORed with 0x80 before sending, here it's 0xA - [Authentication Protocol](https://github.com/kinnay/NintendoClients/wiki/Authentication-Protocol)
- `04 00 00 00` - RMC call ID (incremented), shared for the request and response, here 4
- `01 00 00 00` - RMC method ID, here 1

Having understood protocol and method IDs we can conclude that the packet is a request for [(1) Login](https://github.com/kinnay/NintendoClients/wiki/Authentication-Protocol#1-login) method of the authentication service - usually the first RMC packet to be received in any Quazal-built game.

## RMC Payload

Now all there is left to do is interpret the data the request carries:
```
06 00 6D 69 6D 61 6B 00
```

Every method has its own RMC payload structure, which consists of the SDK's [common data types](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types).

Standard data types and services are well-documented at [github.com/kinnay/NintendoClients/wiki](https://github.com/kinnay/NintendoClients/wiki/). If we take a look at authentication service and [(1) Login](https://github.com/kinnay/NintendoClients/wiki/Authentication-Protocol#1-login) method, it says we should interpret the data as a [string](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) with the username which the server is going to authenticate.

Following the string encoding we can break it down:
- `06 00` - the length of the string (including null terminator)
- `6D 69 6D 61 6B 00` - null-terminated username - `mimak`

Note that at some point the games usually use their own objects which are serialized into RMC packets of custom-made RMC services. Those need to be reverse engineered from the binary and documented unless there's a similiar service already documented for a different game like GRP/GRFS - then they **still need to be compared** as changes could have been applied between the two releases.

# ACB RMC services
Below you can find the list of all RMC services present in both of the AC Brothehood's binaries.

Note that not all of these services (especially OSDK ones) are used by the game, some are just leftover dependencies of the SDK.

| ID (hex) | Service | Service type | Engine module |
|---|---|---|---|
| 01 | [Remote Log Device](https://github.com/kinnay/NintendoClients/wiki/Remote-Log-Device-Protocol) | client and server | OSDK |
| 03 | [NAT Traversal](https://github.com/kinnay/NintendoClients/wiki/NAT-Traversal-Protocol) | client and server | OSDK |
| 0A | [Authentication](https://github.com/kinnay/NintendoClients/wiki/Authentication-Protocol) | client | OSDK |
| 0B | [Secure](https://github.com/kinnay/NintendoClients/wiki/Secure-Protocol) | client | OSDK |
| 0E | [Notifications](https://gitlab.com/phoenix-network-ltd/ac-brotherhood-docs/-/wikis/RMC-Notification-Protocol) | server | OSDK |
| 12 | [Health](https://github.com/kinnay/NintendoClients/wiki/Health-Protocol) | client | OSDK |
| 13 | [Monitoring](https://github.com/kinnay/NintendoClients/wiki/Monitoring-Protocol) | client | OSDK |
| 14 | [Friends](https://github.com/kinnay/NintendoClients/wiki/Friends-Protocol) | client | OSDK |
| 15 | [Matchmaking](https://github.com/kinnay/NintendoClients/wiki/Match-Making-Protocol) | client | OSDK |
| 17 | [Messaging](https://github.com/kinnay/NintendoClients/wiki/Messaging-Protocol) | client | OSDK |
| 18 | [Persistent Store](https://gitlab.com/phoenix-network-ltd/ac-brotherhood-docs/-/wikis/RMC-Persistent-Store-Protocol) | client | OSDK |
| 19 | [Account Mgmt](https://github.com/kinnay/NintendoClients/wiki/Account-Management-Protocol) | client | OSDK |
| 1B | [Message Delivery](https://github.com/kinnay/NintendoClients/wiki/Message-Delivery-Protocol) | client and server | OSDK |
| 1D | [Ubi Account Mgmt](https://gitlab.com/phoenix-network-ltd/ac-brotherhood-docs/-/wikis/RMC-Ubi-Account-Management-Protocol) | client | OSDK (Ubi games) |
| 1F | [News](https://github.com/kinnay/NintendoClients/wiki/News-Protocol) | client | OSDK |
| 20 | News Admin | client | OSDK |
| 21 | [Ubi News](https://gitlab.com/phoenix-network-ltd/ac-brotherhood-docs/-/wikis/RMC-Ubi-News-Protocol) | client | OSDK (Ubi games) |
| 23 | [Privileges](https://gitlab.com/phoenix-network-ltd/ac-brotherhood-docs/-/wikis/RMC-Privileges-Protocol) | client | OSDK |
| 24 | [Tracking](https://gitlab.com/phoenix-network-ltd/ac-brotherhood-docs/-/wikis/RMC-Tracking-Protocol) | client | OSDK |
| 27 | [Localization](https://github.com/kinnay/NintendoClients/wiki/Localization-Protocol) | client | OSDK |
| 28 | Localization Admin | client | OSDK |
| 2A | [Game Session](https://github.com/kinnay/NintendoClients/wiki/Game-Session-Protocol) | client | OSDK |
| 2B | Game Session Admin | client | OSDK |
| 32 | [Matchmaking Extended](https://github.com/kinnay/NintendoClients/wiki/Match-Making-Protocol-Ext) | client | OSDK |
| 65 | [Player Stats]() | client | |
| 6C | [Hermes Player Statistics](https://gitlab.com/phoenix-network-ltd/ac-brotherhood-docs/-/wikis/RMC-Player-Statistics-Protocol) | client | Hermes |
| 6D | [Rich Presence](https://gitlab.com/phoenix-network-ltd/ac-brotherhood-docs/-/wikis/RMC-Rich-Presence-Protocol) | client | Hermes |
| 6E | [Clans](https://gitlab.com/phoenix-network-ltd/ac-brotherhood-docs/-/wikis/RMC-Clans-Protocol) | client | Hermes |
| 6F | [Tracking Extension](https://gitlab.com/phoenix-network-ltd/ac-brotherhood-docs/-/wikis/RMC-Tracking-Extension-Protocol) | client | |
| 70 | [Meta Session](https://gitlab.com/phoenix-network-ltd/ac-brotherhood-docs/-/wikis/RMC-Meta-Session-Protocol) | client | Hermes |
| 71 | [Game Info](https://gitlab.com/phoenix-network-ltd/ac-brotherhood-docs/-/wikis/RMC-Game-Info-Protocol) | client | Hermes |
| 72 | [Contacts](https://gitlab.com/phoenix-network-ltd/ac-brotherhood-docs/-/wikis/RMC-Contacts-Protocol) | client | Hermes |
| 74 | [Hermes Achievements](https://gitlab.com/phoenix-network-ltd/ac-brotherhood-docs/-/wikis/RMC-Hermes-Achievements-Protocol) | client | Hermes |
| 75 | [Social Networks](https://gitlab.com/phoenix-network-ltd/ac-brotherhood-docs/-/wikis/RMC-Social-Networks-Protocol) | client | Hermes |
| 76 | [Virgin](https://gitlab.com/phoenix-network-ltd/ac-brotherhood-docs/-/wikis/RMC-Virgin-Protocol) | client | Scimitar |
| 77 | [Leaderboard]() | client | |
| 78 | [Uplay Win](https://gitlab.com/phoenix-network-ltd/ac-brotherhood-docs/-/wikis/RMC-Uplay-Win-Protocol) | client | |
| 79 | [Facebook]() | client | |
| 7A | [Shop Renting]() | client | |