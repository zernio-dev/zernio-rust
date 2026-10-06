# WebhookPayloadContactTag

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Event id, the dedupe key. | 
**event** | **Event** |  (enum: contact.tag_added, contact.tag_removed) | 
**timestamp** | **String** |  | 
**contact** | [**models::WebhookPayloadContactTagContact**](WebhookPayloadContactTagContact.md) |  | 
**tag** | **String** |  | 
**source** | **Source** | Who wrote the tag: the API or dashboard, a workflow add_tag / remove_tag node, or a comment-automation link click. (enum: api, workflow, automation) | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


