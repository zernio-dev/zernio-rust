# WebhookPayloadSequenceEnrollment

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Event id, the dedupe key. | 
**event** | **Event** |  (enum: sequence.enrolled, sequence.exited) | 
**timestamp** | **String** |  | 
**sequence** | [**models::UpdateFacebookPage200ResponseSelectedPage**](UpdateFacebookPage200ResponseSelectedPage.md) |  | 
**contact** | [**models::WebhookPayloadContactTagContact**](WebhookPayloadContactTagContact.md) |  | 
**enrollment** | [**models::CreateTestLead200ResponseTestLead**](CreateTestLead200ResponseTestLead.md) |  | 
**exit_reason** | Option<**ExitReason**> | sequence.exited only. completed: the last step was sent; replied: the contact replied and the sequence exits on reply; manual: unenrolled through the API; failed: the step kept failing to send; unsubscribed: the contact opted out. (enum: completed, replied, manual, failed, unsubscribed) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


