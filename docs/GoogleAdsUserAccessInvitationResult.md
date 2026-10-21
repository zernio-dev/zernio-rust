# GoogleAdsUserAccessInvitationResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**customer_id** | Option<**String**> |  | [optional]
**email_address** | Option<**String**> |  | [optional]
**access_role** | Option<[**models::GoogleAdsAccessRole**](GoogleAdsAccessRole.md)> |  | [optional]
**status** | Option<**Status**> | PENDING once the email is sent; PENDING_APPROVAL while Google waits for a second admin's multi-party approval. (enum: PENDING, PENDING_APPROVAL) | [optional]
**invitation_id** | Option<**String**> | Null on validateOnly and while the invitation awaits multi-party approval. | [optional]
**multi_party_auth_review_id** | Option<**String**> | Google's multi-party approval review id when status is PENDING_APPROVAL. | [optional]
**validate_only** | Option<**bool**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


