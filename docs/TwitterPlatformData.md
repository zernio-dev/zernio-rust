# TwitterPlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**article** | Option<[**models::XArticle**](XArticle.md)> |  | [optional]
**reply_to_tweet_id** | Option<**String**> | ID of an existing tweet to reply to. The published tweet will appear as a reply in that tweet's thread. For threads, only the first tweet replies to the target; subsequent tweets chain normally. X only permits replying to your own posts or posts you are mentioned in; replying to an arbitrary other account's post is rejected by X. | [optional]
**quote_tweet_id** | Option<**String**> | ID (or full status URL) of an existing tweet to quote-repost. The published tweet becomes a quote tweet of the target. Mutually exclusive with media and poll. X only permits quoting your own posts or posts you are mentioned in / part of the conversation thread of; quoting an arbitrary other account's post is rejected by X. Billed at the standard create rate ($0.015), unlike pasting a tweet URL into the text which is billed at the URL rate ($0.20). For threads, applies to the first tweet only. | [optional]
**reply_settings** | Option<**ReplySettings**> | Controls who can reply to the tweet. \"following\" allows only people you follow, \"mentionedUsers\" allows only mentioned users, \"subscribers\" allows only subscribers, \"verified\" allows only verified users. Omit for default (everyone can reply). For threads, applies to the first tweet only. Cannot be combined with replyToTweetId. (enum: following, mentionedUsers, subscribers, verified) | [optional]
**thread_items** | Option<[**Vec<models::TwitterPlatformDataThreadItemsInner>**](TwitterPlatformDataThreadItemsInner.md)> | Complete sequence of tweets in a thread. The first item becomes the root tweet, subsequent items are chained as replies. When threadItems is provided, the top-level content field is used only for display and search purposes, it is NOT published. You must include your first tweet as threadItems[0].  | [optional]
**poll** | Option<[**models::TwitterPlatformDataPoll**](TwitterPlatformDataPoll.md)> |  | [optional]
**long_video** | Option<**bool**> | Uploads the video with X's amplify_video media category instead of the standard tweet_video. Applied only when the connected X account has a paid X subscription; on other accounts the flag is accepted and ignored. It is not required to post long videos. The standard tweet_video path already publishes videos well past 140 seconds on free accounts, and maximum duration is set by X per account, not by Zernio. Zernio enforces only the 512 MB file-size limit. Some accounts additionally require X's long-video API allowlisting, without which X rejects an amplify_video upload. | [optional][default to false]
**geo_restriction** | Option<[**models::GeoRestriction**](GeoRestriction.md)> |  | [optional]
**paid_partnership** | Option<**bool**> | When true, the post is labeled by X as a paid partnership / paid promotion. For threads, applies to the root tweet only. Field availability may depend on your X API access tier. | [optional][default to false]
**made_with_ai** | Option<**bool**> | When true, the post is labeled by X as containing AI-generated media. Per X, this label is for AI-generated media, not AI-written text. For threads, applies to the root tweet only. | [optional][default to false]
**sensitive_media** | Option<[**models::TwitterPlatformDataSensitiveMedia**](TwitterPlatformDataSensitiveMedia.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


