# CreateImapAccountRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** |  | 
**email** | **String** |  | 
**name** | Option<**String**> | Shown to people the mailbox emails. | [optional]
**password** | Option<**String**> | Shortcut for imap.password. | [optional]
**imap** | Option<[**models::CreateImapAccountRequestImap**](CreateImapAccountRequestImap.md)> |  | [optional]
**smtp** | Option<[**models::CreateImapAccountRequestSmtp**](CreateImapAccountRequestSmtp.md)> |  | [optional]
**identities** | Option<[**Vec<models::CreateImapAccountRequestIdentitiesInner>**](CreateImapAccountRequestIdentitiesInner.md)> | Other addresses this mailbox sends as. | [optional]
**dry_run** | Option<**bool**> | Run every check and store nothing, for live validation in your own form. | [optional]
**allow_self_signed_certificate** | Option<**bool**> | On-premise servers only: accept a certificate that cannot be verified. The hosted page never offers it. | [optional]
**reconnect_account_id** | Option<**String**> | Reconnect this account in place with a new password; the stored servers are reused. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


