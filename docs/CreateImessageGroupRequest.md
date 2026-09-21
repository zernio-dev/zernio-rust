# CreateImessageGroupRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | The iMessage account (sender) that opens the group | 
**contacts** | **Vec<String>** | Participant handles (E.164 phones or iMessage emails) | 
**text** | **String** | The first message | 
**name** | Option<**String**> | Group name (required for WhatsApp groups) | [optional]
**channel** | Option<**Channel**> |  (enum: imessage, sms, rcs, whatsapp) | [optional][default to Imessage]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


