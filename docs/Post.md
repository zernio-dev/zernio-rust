# Post

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | Option<**String**> |  | [optional]
**user_id** | Option<[**models::PostUserId**](PostUserId.md)> |  | [optional]
**title** | Option<**String**> | Stored on the post for reference/display only. This field is NOT used as the video title when publishing. To set a YouTube video title, use platformSpecificData.title on the youtube platform target (falls back to the first line of content when omitted). | [optional]
**content** | Option<**String**> |  | [optional]
**media_items** | Option<[**Vec<models::MediaItem>**](MediaItem.md)> |  | [optional]
**platforms** | Option<[**Vec<models::PlatformTarget>**](PlatformTarget.md)> |  | [optional]
**scheduled_for** | Option<**String**> |  | [optional]
**timezone** | Option<**String**> |  | [optional]
**status** | Option<**Status**> |  (enum: draft, scheduled, publishing, published, failed, partial) | [optional]
**tags** | Option<**Vec<String>**> | YouTube constraints: each tag max 100 chars, combined max 500 chars, duplicates removed. | [optional]
**hashtags** | Option<**Vec<String>**> | Stored for reference only. Hashtags are NOT automatically appended to the caption when publishing. Include hashtags directly in the content field (platforms like Instagram only support hashtags as caption text). For YouTube keywords, use the tags field instead. | [optional]
**mentions** | Option<**Vec<String>**> | Stored for reference only. This field does NOT automatically create @mentions when publishing. For LinkedIn @mentions, use the /v1/accounts/{accountId}/linkedin-mentions endpoint to resolve profile URLs to URNs, then embed the returned mentionFormat directly in the post content field. | [optional]
**visibility** | Option<**Visibility**> |  (enum: public, private, unlisted) | [optional]
**metadata** | Option<**std::collections::HashMap<String, serde_json::Value>**> |  | [optional]
**recycling** | Option<[**models::RecyclingState**](RecyclingState.md)> |  | [optional]
**recycled_from_post_id** | Option<**String**> | ID of the original post if this post was created via recycling | [optional]
**queued_from_profile** | Option<**String**> | Profile ID if the post was scheduled via the queue | [optional]
**queue_id** | Option<**String**> | Queue ID if the post was scheduled via a specific queue | [optional]
**created_at** | Option<**String**> |  | [optional]
**updated_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


