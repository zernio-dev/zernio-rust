# WebhookPayloadCommentCommentAuthor

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Author's platform ID | 
**username** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**picture** | Option<**String**> |  | [optional]
**is_own_account** | Option<**bool**> | True when this comment was authored by the connected account itself (Meta re-delivers the account's own replies as comments events). Populated on the Instagram and Facebook realtime webhooks only; absent means not evaluated, never \"not the account\". | [optional]
**instagram_profile** | Option<[**models::WebhookPayloadCommentCommentAuthorInstagramProfile**](WebhookPayloadCommentCommentAuthorInstagramProfile.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


