[Notification protocol](https://github.com/kinnay/NintendoClients/wiki/Notification-Protocol) is the OSDK-native event system for RDV to notify the game of online events. The notifications are sent by the server as [`Quazal::NotificationEvent`](https://github.com/kinnay/NintendoClients/wiki/Notification-Protocol#notificationevent-structure) objects inside of RMC payloads.

# ACB Notifications

In ACB notification events are processed in `Hermes::PlatformListenerServiceRDV::ProcessNotificationEvent` (0x1E4F710).

| Type | Subtype | Param2 | Notification | OnlineEventData ID |
|------|---------|--------|--------------|-----------------|
| 1 | any | 0 | OnlineEventDataFriendshipAnswered | 19 |
| 1 | any | 1 | OnlineEventDataFriendshipAnswered | 18 |
| 1 | any | 2 | OnlineEventDataFriendshipRequested | 16 |
| 3 | 1 | any | OnlineEventCustomRDV | 21 |
| 3 | 2, 8 | any | OnlineEventCustomRDV | 22 |
| 3 | 3 | any | unknown | none |
| 5 | any | any | OnlineEventDataFriendStatus | 15 |
| 6 | any | any | OnlineEventData | 32 |
| 7 | 5 | any | OnlineEventDataInvitation | 23 |
| 7 | 7 | any | OnlineEventDataInvitation | 25 |
| 7 | 8 | any | OnlineEventDataInvitation | 26 |
| 7 | 9 | any | OnlineEventDataInvitation | 27 |
| 7 | default | any | OnlineEventCustomRDV | 29 |
| 1000 | any | any | OnlineEventCustomRDV | 31 |
| 1001 | any | any | OnlineEventSwissRoundTournament | 33 |
| 1002 | any | any | OnlineEventMetasession | 36 |
| 1003 | any | any | OnlineEventClan | 39 |