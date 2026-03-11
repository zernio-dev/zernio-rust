# TwitterPlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**reply_to_tweet_id** | Option<**String**> | ID of an existing tweet to reply to. The published tweet will appear as a reply in that tweet's thread. For threads, only the first tweet replies to the target; subsequent tweets chain normally. | [optional]
**reply_settings** | Option<**ReplySettings**> | Controls who can reply to the tweet. \"following\" allows only people you follow, \"mentionedUsers\" allows only mentioned users, \"subscribers\" allows only subscribers, \"verified\" allows only verified users. Omit for default (everyone can reply). For threads, applies to the first tweet only. Cannot be combined with replyToTweetId. (enum: following, mentionedUsers, subscribers, verified) | [optional]
**thread_items** | Option<[**Vec<models::TwitterPlatformDataThreadItemsInner>**](TwitterPlatformDataThreadItemsInner.md)> | Sequence of tweets in a thread. First item is the root tweet. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


