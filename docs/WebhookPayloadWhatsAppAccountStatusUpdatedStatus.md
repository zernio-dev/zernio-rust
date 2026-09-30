# WebhookPayloadWhatsAppAccountStatusUpdatedStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **Status** | `active` only on a reinstatement (DISABLED_UPDATE with ban state REINSTATE). (enum: restricted, active) | 
**meta_event** | **String** | Meta `account_update` event: ACCOUNT_RESTRICTION, ACCOUNT_VIOLATION, ACCOUNT_DELETED or DISABLED_UPDATE. | 
**reason** | Option<**String**> | Human-readable summary. Null on reinstatement. | 
**violation_type** | Option<**String**> | ACCOUNT_VIOLATION only, for example SCAM, ADULT. | 
**restrictions** | [**Vec<models::WebhookPayloadWhatsAppAccountStatusUpdatedStatusRestrictionsInner>**](WebhookPayloadWhatsAppAccountStatusUpdatedStatusRestrictionsInner.md) | ACCOUNT_RESTRICTION only. Empty otherwise. | 
**ban_state** | Option<**String**> | DISABLED_UPDATE only (for example DISABLE, REINSTATE). | 
**ban_date** | Option<**String**> | DISABLED_UPDATE only, as Meta sent it (for example \"September 23, 2026\"). | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


