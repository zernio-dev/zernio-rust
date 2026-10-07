# PlatformAnalytics

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | Option<**String**> |  | [optional]
**status** | Option<**Status**> |  (enum: published, failed) | [optional]
**platform_post_id** | Option<**String**> | The native post ID on the platform (e.g. Instagram media ID, tweet ID) | [optional]
**account_id** | Option<**String**> |  | [optional]
**account_username** | Option<**String**> |  | [optional]
**analytics** | Option<[**models::PostAnalytics**](PostAnalytics.md)> |  | [optional]
**sync_status** | Option<**SyncStatus**> | Sync state of analytics for this platform (enum: synced, pending, unavailable) | [optional]
**platform_post_url** | Option<**String**> |  | [optional]
**error_message** | Option<**String**> | Failure detail. On failed entries, why the post failed to publish. On unavailable entries, why analytics cannot be synced (e.g. Google Business Profile, a TikTok upload that never received a video id). On pending entries, the most recent analytics sync error for the account (null while no sync has failed), cleared after the next successful sync. | [optional]
**error_code** | Option<**ErrorCode**> | Stable machine-readable reason for errorMessage. post_not_found: the post was deleted or is no longer visible to the account. not_post_owner: the post is owned by another Page or user (collab or visitor post); its analytics cannot be read with this Page's token. permission_missing: the last analytics sync of the Facebook account failed because the Page no longer grants pages_read_engagement (pending entries only). null: no stable code, read errorMessage. New values may be added. (enum: post_not_found, not_post_owner, permission_missing, ) | [optional]
**is_owner** | Option<**bool**> | Facebook only: true when the connected Page authored the post, false when Facebook reports another author (a collab post), null when unknown or for other platforms. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


