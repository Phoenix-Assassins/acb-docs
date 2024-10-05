# Online events

Processed by internal registered event handlers of `Menu::MultiplayerMenu`.

## Session events
Online events of `SessionEvent::OnlineEventType` enum.

Processed by `Menu::MultiplayerMenu::HandleSessionEvent`(0xEA5140).

| ID | Event |
|:-:|:-:|
| 0 | OnlineEventUndefined |
| 1 | OnlineEventHermesEvent |
| 2 | OnlineEventJoinNetZFinished |
| 3 | OnlineEventLeaveNetZFinished |
| 4 | OnlineEventEnterSession |
| 5 | OnlineEventLeaveSession |
| 6 | OnlineEventEndMatchCleanUpFinished |
| 7 | OnlineEventReadyToRematch |
| 8 | OnlineEventLeavingSession |
| 9 | OnlineEventQuittingSession |
| 10 | OnlineEventMigrationFailed |
| 11 | OnlineEventSearchFinished |
| 12 | OnlineEventCreateFinished |
| 13 | OnlineEventJoinFinished |
| 14 | OnlineEventCancelled |
| 15 | OnlineEventMetaSearchFinished |
| 16 | OnlineEventGroupDefined |
| 17 | OnlineEventBecameGroupLeader |
| 18 | OnlineEventNoMoreGroupLeader |
| 19 | OnlineEventBecameSessionLeader |
| 20 | OnlineEventNoMoreSessionLeader |
| 21 | OnlineEventBecameBusy |
| 22 | OnlineEventNoLongerBusy |
| 23 | OnlineEventStateChanged |
| 24 | OnlineEventUpdateFriendListInProgress |
| 25 | OnlineEventUpdatedFriendList |
| 26 | OnlineEventGetGameInfoFinished |
| 27 | OnlineEventChangeSessionFinished |
| 28 | OnlineEventMustMerge |
| 29 | OnlineEventSessionObjectReplicated |
| 30 | OnlineEventOnlinePlayersUpdated |
| 31 | OnlineEventSessionInfosUpdated |
| 32 | OnlineEventSendMessage |
| 33 | OnlineEventRetrieveMessages |
| 34 | OnlineEventUpdatedBlockedPlayersList |
| 35 | OnlineEventBlockPlayer |
| 36 | OnlineEventUnblockPlayer |
| 37 | OnlineEventFriendRequestAnswer |
| 38 | OnlineEventUpdatedSentFriendshipRequests |
| 39 | OnlineEventUpdatedIncomingFriendshipRequests |
| 40 | OnlineEventAddFriend |
| 41 | OnlineEventAlreadyFriend |
| 42 | OnlineEventRemoveFriend |
| 43 | OnlineEventRetrieveGameInvites |
| 44 | OnlineEventDeclineGameInvite |
| 45 | OnlineEventCancelledGameInvite |
| 46 | OnlineEventMessagesUpdate |
| 47 | OnlineEventRecentPlayersUpdate |
| 48 | OnlineEventReceivedNewGameInvite |
| 49 | OnlineEventPbKick |
| 50 | OnlineEventPlayerAlreadyBlocked |
| 51 | OnlineEventBecomeIdle |
| 52 | OnlineEventActivateRDV |
| 53 | OnlineEventDesactivateRDV |
| 54 | OnlineEventForceReturnMainMenu |
| 55 | OnlineEventBecomePlaying |
| 56 | OnlineEventUpdatedLeaderboard |
| 57 | OnlineEventUpdatedStatistics |
| 58 | OnlineEventGetNewsChannelsFinished |
| 59 | OnlineEventGetNewsHeadersFinished |
| 60 | OnlineEventGetNewsBodiesFinished |
| 61 | OnlineEventGetNewsCountFinished |
| 62 | OnlineEventSendRankingStarted |
| 63 | OnlineEventSendRankingFinished |
| 64 | OnlineEventSendRankingLevelUpStarted |
| 65 | OnlineEventSendRankingLevelUpFinished |
| 66 | OnlineEventMyGamerCardRetrieved |
| 67 | OnlineEventGamerCardsRetrieved |
| 68 | OnlineEventValidateChallengeStarted |
| 69 | OnlineEventValidateChallengeFinished |
| 70 | OnlineEventMetasessionUpdateTimer |
| 71 | OnlineEventGameInviteSent |
| 72 | OnlineEventMatchmakingStateUpdated |
| 73 | OnlineEventMostPlayedGameMode |
| 74 | OnlineEventReservationInProgress |
| 75 | OnlineEventReservationAccepted |
| 76 | OnlineEventReservationDenied |
| 77 | OnlineEventGroupUpdated |
| 78 | OnlineEventAllGroupMembersJoining |
| 79 | OnlineEventAllSessionMembersJoining |
| 80 | OnlineEventGroupJoined |
| 81 | OnlineEventGroupCreated |
| 82 | OnlineEventCXBLoaded |
| 83 | OnlineEventBlockListUpdated |
| 84 | OnlineEventUpdatedTemplarPyramidInfo |
| 85 | OnlineEventPlayerAdded |
| 86 | OnlineEventPlayerRemoved |
| 87 | OnlineEventPlayerUpdated |

## UI events

The events of `UIMultiEvent_MultiplayerMenu::EventType` enum.


Processed by `Menu::MultiplayerMenu::HandleUIEvent`(0xEA4B30).

| ID | Event |
|:-:|:-:|
| 0 | MultiplayerMenuShowing |
| 1 | MultiplayerMenuHiding |
| 2 | MultiplayerMenuShowingWithHUD |
| 3 | MultiplayerMenuHidingWithHUD |
| 4 | MultiplayerMenuLoginFailed |
| 5 | MultiplayerMenuLoginSucceeded |
| 6 | MultiplayerMenuConnectionDropped |
| 7 | MultiplayerMenuCableDisconnected |