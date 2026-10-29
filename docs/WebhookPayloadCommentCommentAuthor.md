# WebhookPayloadCommentCommentAuthor

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Author's platform ID | 
**username** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**picture** | Option<**String**> |  | [optional]
**is_own_account** | Option<**bool**> | True when this comment was authored by the connected account itself. Absent means not evaluated, never \"not the account\".  - Instagram and Facebook realtime webhooks: populated (Meta re-delivers the account's own replies as comments events). - TikTok: inferred. Comments created through this API are always flagged, and once the account's own author identifier is known (from one of those or from a comments listing), every author is compared against it.  | [optional]
**instagram_profile** | Option<[**models::WebhookPayloadCommentCommentAuthorInstagramProfile**](WebhookPayloadCommentCommentAuthorInstagramProfile.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


