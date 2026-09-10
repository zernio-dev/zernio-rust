# GetAdComments200ResponseMeta

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **Platform** | Platform of the comments. (enum: facebook, instagram, tiktok) | 
**placement** | Option<**Placement**> | The placement these comments are for, useful when you didn't pass ?placement= and want to know which one you got. (enum: facebook, instagram) | [optional]
**ad_id** | **String** | Internal Zernio ad ID. | 
**platform_ad_id** | Option<**String**> | Platform ad ID. | [optional]
**effective_story_id** | Option<**String**> | Underlying post ID the comments belong to. effective_object_story_id for the Facebook side, effective_instagram_media_id for the Instagram side. | [optional]
**tiktok_item_id** | Option<**String**> | TikTok-only video item ID from stored ad fields or returned comments. Null does not prevent listing; ad details are not fetched to populate it. | [optional]
**since** | Option<[**String**](String.md)> | TikTok-only resolved start date. | [optional]
**until** | Option<[**String**](String.md)> | TikTok-only resolved end date. | [optional]
**facebook_account_id** | Option<**String**> | Facebook-only. The connected Facebook Page SocialAccount these comments were read through. Pass it as `accountId` (with `effectiveStoryId` as the postId) to /v1/inbox/comments to reply/hide/delete. Null when no connected Page was used (then moderation isn't possible). | [optional]
**instagram_user_id** | Option<**String**> | Instagram-only. The Instagram-scoped business ID that owns the boosted media (creative.instagram_user_id). | [optional]
**instagram_permalink** | Option<**String**> | Instagram-only. Public permalink of the boosted IG post (creative.instagram_permalink_url). | [optional]
**instagram_account_id** | Option<**String**> | Instagram-only. The connected Instagram SocialAccount these comments were read through. Pass it as `accountId` (with `effectiveStoryId` as the postId) to /v1/inbox/comments to reply/hide/delete. | [optional]
**account_id** | **String** | Account ID (ads SocialAccount). | 
**last_updated** | **String** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


