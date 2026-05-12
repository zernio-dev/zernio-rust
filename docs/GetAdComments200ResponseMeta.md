# GetAdComments200ResponseMeta

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **Platform** | Which side these comments are on (same as `placement`). (enum: facebook, instagram) | 
**placement** | **Placement** | The placement these comments are for — useful when you didn't pass ?placement= and want to know which one you got. (enum: facebook, instagram) | 
**ad_id** | **String** | Internal Zernio ad ID. | 
**platform_ad_id** | **String** | Meta ad ID. | 
**effective_story_id** | **String** | Underlying post ID the comments belong to. effective_object_story_id for the Facebook side, effective_instagram_media_id for the Instagram side. | 
**facebook_account_id** | Option<**String**> | Facebook-only. The connected Facebook Page SocialAccount these comments were read through — pass it as `accountId` (with `effectiveStoryId` as the postId) to /v1/inbox/comments to reply/hide/delete. Null when no connected Page was used (then moderation isn't possible). | [optional]
**instagram_user_id** | Option<**String**> | Instagram-only. The Instagram-scoped business ID that owns the boosted media (creative.instagram_user_id). | [optional]
**instagram_permalink** | Option<**String**> | Instagram-only. Public permalink of the boosted IG post (creative.instagram_permalink_url). | [optional]
**instagram_account_id** | Option<**String**> | Instagram-only. The connected Instagram SocialAccount these comments were read through — pass it as `accountId` (with `effectiveStoryId` as the postId) to /v1/inbox/comments to reply/hide/delete. | [optional]
**account_id** | **String** | Social account ID (ads SocialAccount). | 
**last_updated** | **String** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


