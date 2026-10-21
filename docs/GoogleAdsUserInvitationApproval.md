# GoogleAdsUserInvitationApproval

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**multi_party_auth_review_id** | Option<**String**> | Pass to DELETE /v1/ads/accounts/user-invitations/pending-approvals to withdraw the request. | [optional]
**email_address** | Option<**String**> | Invited email address. | [optional]
**access_role** | Option<**AccessRole**> |  (enum: ADMIN, STANDARD, READ_ONLY, EMAIL_ONLY, UNKNOWN) | [optional]
**request_user_email** | Option<**String**> | Google user who sent the invitation. Only this user can withdraw it. | [optional]
**created_at** | Option<**String**> | Google's creation time, yyyy-MM-dd HH:mm:ss.ssssss in the account's time zone. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


