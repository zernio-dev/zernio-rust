# WebhookPayloadContactFieldChanged

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Event id, the dedupe key. | 
**event** | **Event** |  (enum: contact.field_changed) | 
**timestamp** | **String** |  | 
**contact** | [**models::WebhookPayloadContactTagContact**](WebhookPayloadContactTagContact.md) |  | 
**field** | **String** | Custom field slug. | 
**previous_value** | Option<**serde_json::Value**> |  | 
**value** | Option<**serde_json::Value**> |  | 
**source** | **Source** | Who wrote the field: the API or dashboard, a workflow set_field node, or an automation. (enum: api, workflow, automation) | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


