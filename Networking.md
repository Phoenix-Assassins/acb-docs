This page describes the general idea of the networking solution and systems used by the game.

# Overview
The game communicates with services of:
- Ubisoft Connect (Uplay)
- ubi.com
- Quazal game servers

# Subsections
 For specific information on networking see [GRO wikis](https://github.com/zeroKilo/GROBackendWV/wiki) and pages listed below.
- [HTTP](https://github.com/zeroKilo/GROBackendWV/wiki/TCP-Webrequests)
- [PRUDP](https://github.com/zeroKilo/GROBackendWV/wiki/PRUDP-Quazal-NetZ)
- [RMC](/RMC.md)
- [RC4 encryption](https://github.com/zeroKilo/GROBackendWV/wiki/QPacket-Encryption)
- [Zlib compression](https://github.com/zeroKilo/GROBackendWV/wiki/QPacket-Compression)
- [Duplicated Objects](https://github.com/zeroKilo/GROBackendWV/wiki/DO)
- [DO RMC](https://github.com/zeroKilo/GROBackendWV/wiki/DO-RMC-Calls)


# General flow
When a player launches a game, first it communicates with Ubisoft Connect services via `ubiorbitapi_r2_loader.dll` to verify the access to a copy of the game. Little is known of Ubisoft's ORBITAPI and Uplay DRM services and as they are going to remain live, they are out of scope of this project. An original copy of the game linked to a Ubisoft account is required.

The game consists of 2 executables:
- ACBSP.exe (singleplayer)
- ACBMP.exe (multiplayer)

The singleplayer binary is launched initially, when a player chooses multiplayer mode from the menu it's closed and the multiplayer version launches.

While multiplayer menu is loading, the game sends HTTP request to ubi.com, requesting URLs and configuration for [PRUDP (pretty reliable UDP)](https://github.com/zeroKilo/GROBackendWV/wiki/PRUDP-Quazal-NetZ) game servers. Example request and response (from the live service - July 9 2022) are shown below.

## HTTP request

```
GET /OnlineConfigService.svc/GetOnlineConfig?onlineConfigID=f26ad290e85146a685acbbb5f6ed7672&target=client HTTP/1.1
Accept: */*
Cookie: 
Host: onlineconfigservice.ubi.com
```

## HTTP response
### Headers
```
HTTP/1.1 200 OK
Cache-Control: private
Content-Length: 733
Content-Type: application/json; charset=utf-8
Server: Microsoft-IIS/7.5
X-AspNet-Version: 2.0.50727
X-Powered-By: ASP.NET
Date: Sat, 09 Jul 2022 21:10:34 GMT
```
### Body
```json
[
   {
      "Name":"SandboxUrl",
      "Values":[
         "prudp:\/address=mdc-mm-rdv57.ubisoft.com;port=23990"
      ]
   },
   {
      "Name":"SandboxUrlWS",
      "Values":[
         "mdc-mm-rdv57.ubisoft.com:23990"
      ]
   },
   {
      "Name":"uplay_DownloadServiceUrl",
      "Values":[
         "https:\/\/secure.ubi.com\/UplayServices\/UplayFacade\/DownloadServicesRESTXML.svc\/REST\/XML\/?url="
      ]
   },
   {
      "Name":"uplay_DynContentBaseUrl",
      "Values":[
         "http:\/\/static8.cdn.ubi.com\/u\/Uplay\/"
      ]
   },
   {
      "Name":"uplay_DynContentSecureBaseUrl",
      "Values":[
         "http:\/\/static8.cdn.ubi.com\/"
      ]
   },
   {
      "Name":"uplay_PackageBaseUrl",
      "Values":[
         "http:\/\/static8.cdn.ubi.com\/u\/Uplay\/Packages\/1.0.3-RC-Shop\/"
      ]
   },
   {
      "Name":"uplay_WebServiceBaseUrl",
      "Values":[
         "https:\/\/secure.ubi.com\/UplayServices\/UplayFacade\/ProfileServicesFacadeRESTXML.svc\/REST\/"
      ]
   }
]
```
`SandboxUrl` points to available PRUDP authentication server, which performs [Kerberos authentication](https://github.com/zeroKilo/GROBackendWV/wiki/Kerberos) and if successful redirects to the secure PRUDP server, often called Rendez-Vous (RDV). RDV is responsible for matchmaking and any other services available from the multiplayer menu.

After successful matchmaking the game begins and RDV redirects the game's traffic to a PRUDP dedicated game server. When the player exits to menu, they are redirected back to RDV.


# Architecture
The servers needed to emulate the network traffic:
- HTTP server with `/OnlineConfigService.svc/GetOnlineConfig` endpoint - original domain `onlineconfigservice.ubi.com` should be redirected to the target domain, preferably by Windows `hosts` file entry
- UDP authentication server - ticket-granting PRUDP server on the port sent in `SandboxUrl`
- UDP RDV server - main backend PRUDP server, port number is that of `SandboxUrl` incremented by 1
- UDP dedicated game server - PRUDP game server, PRUDP URL is sent to the game by RDV's matchmaking service

# Protocols
The game shares PRUDP protocol stack with `Tom Clancy's Ghost Recon Online` which is available [here](https://github.com/zeroKilo/GROBackendWV/wiki/Overview#layers-of-protocols).

Note that the dedicated server's protocols above DO RMC will differ as ACB is a different game built with a different engine.

The highest-layer known protocols for the above servers are:
- HTTP server - HTTP, no SSL, response in JSON format
- UDP authentication server - Quazal's [RMC (Remote Method Calls)](https://github.com/zeroKilo/GROBackendWV/wiki/RMC)
- UDP RDV server - Quazal's [RMC (Remote Method Calls)](https://github.com/zeroKilo/GROBackendWV/wiki/RMC)
- UDP dedicated game server - Quazal's [DO RMC (Duplicated Objects RMC)](https://github.com/zeroKilo/GROBackendWV/wiki/DO-RMC-Calls)