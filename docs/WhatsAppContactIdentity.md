# WhatsAppContactIdentity

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**phone_number** | Option<**String**> | The user's WhatsApp phone number (wa_id), null when Meta did not send it (a username adopter who hides it). | 
**business_scoped_user_id** | Option<**String**> | Meta business-scoped user id (BSUID), for example `US.13491208655302741918`. | 
**parent_business_scoped_user_id** | Option<**String**> | Parent BSUID, shared across the businesses of one portfolio when Meta sends it. | 
**whatsapp_username** | Option<**String**> | The user's WhatsApp username, when Meta sent one with the change. Null on `previous`. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


