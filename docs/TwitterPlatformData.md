# TwitterPlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**reply_to_tweet_id** | Option<**String**> | ID of an existing tweet to reply to. The published tweet will appear as a reply in that tweet's thread. For threads, only the first tweet replies to the target; subsequent tweets chain normally. | [optional]
**reply_settings** | Option<**ReplySettings**> | Controls who can reply to the tweet. \"following\" allows only people you follow, \"mentionedUsers\" allows only mentioned users, \"subscribers\" allows only subscribers, \"verified\" allows only verified users. Omit for default (everyone can reply). For threads, applies to the first tweet only. Cannot be combined with replyToTweetId. (enum: following, mentionedUsers, subscribers, verified) | [optional]
**thread_items** | Option<[**Vec<models::TwitterPlatformDataThreadItemsInner>**](TwitterPlatformDataThreadItemsInner.md)> | Complete sequence of tweets in a thread. The first item becomes the root tweet, subsequent items are chained as replies. When threadItems is provided, the top-level content field is used only for display and search purposes, it is NOT published. You must include your first tweet as threadItems[0].  | [optional]
**poll** | Option<[**models::TwitterPlatformDataPoll**](TwitterPlatformDataPoll.md)> |  | [optional]
**long_video** | Option<**bool**> | Enable long video uploads (over 140 seconds) using amplify_video media category. Requires the connected X account to have an active X Premium subscription. When true, videos are uploaded with the amplify_video category which supports longer durations (up to 10 minutes via API). When false or omitted, the standard tweet_video category is used (140 second limit). Note that not all Premium accounts have API long-video access, as X may require separate allowlisting. | [optional][default to false]
**geo_restriction** | Option<[**models::GeoRestriction**](GeoRestriction.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


