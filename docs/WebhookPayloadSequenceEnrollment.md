# WebhookPayloadSequenceEnrollment

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**test** | Option<**bool**> | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional]
**id** | **String** | Event id, the dedupe key. | 
**profiles** | Option<[**Vec<models::WebhookProfilesInner>**](WebhookProfilesInner.md)> | The profiles this event belongs to, each with the externalId you set on it (null when none is set). Use it to route the event to your tenant without storing Zernio profile ids.  Present on every event tied to a profile, absent on events that belong to none. Events spanning several profiles (a post published to accounts of different profiles) list each once.  | [optional]
**event** | **Event** |  (enum: sequence.enrolled, sequence.exited) | 
**timestamp** | **String** |  | 
**sequence** | [**models::UpdateFacebookPage200ResponseSelectedPage**](UpdateFacebookPage200ResponseSelectedPage.md) |  | 
**contact** | [**models::WebhookPayloadContactTagContact**](WebhookPayloadContactTagContact.md) |  | 
**enrollment** | [**models::CreateTestLead200ResponseTestLead**](CreateTestLead200ResponseTestLead.md) |  | 
**exit_reason** | Option<**ExitReason**> | sequence.exited only. completed: the last step was sent; replied: the contact replied and the sequence exits on reply; manual: unenrolled through the API; failed: the step kept failing to send; unsubscribed: the contact opted out. (enum: completed, replied, manual, failed, unsubscribed) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


