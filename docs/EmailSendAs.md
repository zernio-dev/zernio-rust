# EmailSendAs

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | Option<**String**> |  | [optional]
**name** | Option<**String**> | Display name used when `fromName` is not given. | [optional]
**r#type** | Option<**Type**> | `primary` is the mailbox's own address, `alias` a provider alias, `shared` a declared address (shared mailbox, delegate or alias). (enum: primary, alias, shared) | [optional]
**verification_status** | Option<**VerificationStatus**> | `pending`: Gmail has not verified the alias, so sends from it are refused. `unverified`: declared and not sent from yet; it becomes `accepted` after its first send. (enum: accepted, pending, unverified) | [optional]
**is_default** | Option<**bool**> | The address the provider picks by default. | [optional]
**source** | Option<**Source**> |  (enum: provider, declared) | [optional]
**reply_to** | Option<**String**> | Gmail alias reply-to address, if set. | [optional]
**signature** | Option<[**models::EmailSendAsSignature**](EmailSendAsSignature.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


