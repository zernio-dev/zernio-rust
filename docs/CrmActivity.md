# CrmActivity

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**object_type** | **ObjectType** | HubSpot `note` or `communication` (WhatsApp, SMS); Salesforce `task`. (enum: note, communication, task) | 
**contact_id** | **String** |  | 
**channel** | **Channel** |  (enum: whatsapp, sms, email, call, meeting, instagram, messenger, telegram, other) | 
**direction** | Option<**Direction**> |  (enum: inbound, outbound, ) | 
**subject** | Option<**String**> |  | 
**body** | **String** |  | 
**occurred_at** | **String** |  | 
**url** | **String** | The Salesforce Task, or the HubSpot contact whose timeline shows it. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


