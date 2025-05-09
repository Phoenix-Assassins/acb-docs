A Ubi OSDK service for news management and configuration.

The definitions come from MacOS version of the game.

| Method ID | Method Name |
|-----------|-------------|
| 1 | [CreateChannel](#1-createchannel) |
| 2 | [DeleteChannel](#2-deletechannel) |
| 3 | [DeleteChannels](#3-deletechannels) |
| 4 | [GetChannels](#4-getchannels) |
| 5 | [GetChannelsByTypes](#5-getchannelsbytypes) |
| 6 | [GetChannelsByIDs](#6-getchannelsbyids) |
| 7 | [UpdateChannel](#7-updatechannel) |
| 8 | [GetNewsFeedLinks](#8-getnewsfeedlinks) |
| 9 | [GetNumberOfNewsFeedLinks](#9-getnumberofnewsfeedlinks) |
| 10 | [LinkNewsFeed](#10-linknewsfeed) |
| 11 | [UnlinkNewsFeeds](#11-unlinknewsfeed) |
| 12 | [DeleteNewsMessages](#12-deletenewsmessages) |
| 13 | [DeleteNewsMessagesByRecipient](#13-deletenewsmessagesbyrecipient) |
| 14 | [GetNewsHeaders](#14-getnewsheaders) |
| 15 | [GetNewsMessages](#15-getnewsmessages) |
| 16 | [GetNumberOfNews](#16-getnumberofnews) |
| 17 | [PublishNews](#17-publishnews) |
| 18 | [ProcessNewsFeedURLSJob](#18-processnewsfeedurlsjob) |
| 19 | [UpdateNewsFeedLink](#19-updatenewsfeedlink) |

# (1) CreateChannel

## Request

| Type | Name |
|------|------|
| [NewsChannel](#newschannel-structure) | channel |

## Response

| Type | Name |
|------|------|
| Uint32 | newsChannelID |

# (2) DeleteChannel

## Request

| Type | Name |
|------|------|
| Uint32 | newsChannelID |

## Response

| Type | Name |
|------|------|
| Bool | %retval% |

# (3) DeleteChannels

## Request

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)\<Uint32> | newsChannelIDs |

## Response

| Type | Name |
|------|------|
| Bool | %retval% |

# (4) GetChannels

## Request

| Type | Name |
|------|------|
| [ResultRange](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#resultrange-structure) | resultRange |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[NewsChannel](#newschannel-structure)> | channels |

# (5) GetChannelsByTypes

## Request

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string)> | newsChannelTypes |
| [ResultRange](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#resultrange-structure) | resultRange |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[NewsChannel](#newschannel-structure)> | channels |

# (6) GetChannelsByIDs

## Request

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)\<Uint32> | newsChannelIDs |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[NewsChannel](#newschannel-structure)> | channels |

# (7) UpdateChannel

## Request

| Type | Name |
|------|------|
| [NewsChannel](#newschannel-structure) | channel |

## Response

| Type | Name |
|------|------|
| Bool | %retval% |

# (8) GetNewsFeedLinks

## Request

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)\<Uint32> | newsChannelIDs |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[NewsFeedLink](#newsfeedlink-structure)> | newsFeedLinks |

# (9) GetNumberOfNewsFeedLinks

## Request

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)\<Uint32> | newsChannelIDs |

## Response

| Type | Name |
|------|------|
| Uint32 | numberOfNewsFeedLinks |

# (10) LinkNewsFeed

## Request

| Type | Name |
|------|------|
| [NewsFeedLink](#newsfeedlink-structure) | newsFeedLink |

## Response

| Type | Name |
|------|------|
| Uint32 | newsFeedLinkID |

# (11) UnlinkNewsFeeds

## Request

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)\<Uint32> | newsFeedLinkIDs |

## Response

| Type | Name |
|------|------|
| Uint32 | numberOfDeletedLinks |

# (12) DeleteNewsMessages

## Request

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)\<Uint32> | newsMessageIDs |

## Response

| Type | Name |
|------|------|
| Uint32 | numberOfDeletedNews |

# (13) DeleteNewsMessagesByRecipient

## Request

| Type | Name |
|------|------|
| [NewsRecipient](#newsrecipient-structure) | recipient |

## Response

| Type | Name |
|------|------|
| Uint32 | numberOfDeletedNews |

# (14) GetNewsHeaders

## Request

| Type | Name |
|------|------|
| [NewsRecipient](#newsrecipient-structure) | recipient |
| [ResultRange](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#resultrange-structure) | range |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[NewsHeader](#newsheader-structure)> | newsHeaders |

# (15) GetNewsMessages

## Request

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)\<Uint32> | newsMessageIDs |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[NewsMessage](#newsmessage-structure)> | newsMessages |

# (16) GetNumberOfNews

## Request

| Type | Name |
|------|------|
| [NewsRecipient](#newsrecipient-structure) | recipient |

## Response

| Type | Name |
|------|------|
| Uint32 | numberOfNews |

# (17) PublishNews

## Request

| Type | Name |
|------|------|
| [NewsMessage](#newsmessage-structure) | newsMessage |

## Response

| Type | Name |
|------|------|
| [NewsMessage](#newsmessage-structure) | modifiedNewsMessage |

# (18) ProcessNewsFeedURLSJob

## Request

This method does not take any parameters.

## Response

This method does not return anything.

# (19) UpdateNewsFeedLink

## Request

| Type | Name |
|------|------|
| [NewsFeedLink](#newsfeedlink-structure) | newsFeedLink |

## Response

This method does not return anything.

# Types

## NewsChannel ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

Extends [`Gathering`](https://github.com/kinnay/NintendoClients/wiki/Match-Making-Types#gathering-structure).

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | name |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | channelType |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | locale |
| Bool | subscribable |

## NewsFeedLink ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | m_ID |
| Uint32 | m_newsChannelID |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_description |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_URL |

## NewsRecipient ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

Alias for `MessageRecipient`.

| Type | Name |
|------|------|
| Uint32 | m_idRecipient |
| Uint32 | m_uiRecipientType |

## NewsHeader ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

Extends `UserMessage` (included).

| Type | Name |
|------|------|
| Uint32 | m_uiID |
| Uint32 | m_idRecipient |
| Uint32 | m_uiRecipientType |
| Uint32 | m_uiParentID |
| Uint32 | m_pidSender |
| [DateTime](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#datetime) | m_receptiontime |
| Uint32 | m_uiLifeTime |
| Uint32 | m_uiFlags |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_strSubject |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | m_strSender |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | link |

## NewsMessage ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

Extends [`NewsHeader`](#newsheader-structure).

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | textbody |
