# WebhookPayloadContactFieldChanged

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**test** | Option<**bool**> | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional]
**id** | **String** | Event id, the dedupe key. | 
**profiles** | Option<[**Vec<models::WebhookProfilesInner>**](WebhookProfilesInner.md)> | The profiles this event belongs to, each with the externalId you set on it (null when none is set). Present on every event tied to a profile and absent on events that belong to none. Events spanning several profiles (a post published to accounts of different profiles) list each once. Use it to route the event to your tenant without storing Zernio profile ids. | [optional]
**event** | **Event** |  (enum: contact.field_changed) | 
**timestamp** | **String** |  | 
**contact** | [**models::WebhookPayloadContactTagContact**](WebhookPayloadContactTagContact.md) |  | 
**field** | **String** | Custom field slug. | 
**previous_value** | Option<**serde_json::Value**> |  | 
**value** | Option<**serde_json::Value**> |  | 
**source** | **Source** | Who wrote the field: the API or dashboard, a workflow set_field node, or an automation. (enum: api, workflow, automation) | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


