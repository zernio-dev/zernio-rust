# WebhookPayloadMessageSentMessageSender

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | The Zernio account id of the connected account that sent the message, not a contact id. | 
**contact_id** | Option<**String**> | Always omitted on this event: the sender is the business, not a contact. Use conversation.contactId to join back to the CRM Contact. | [optional]
**name** | Option<**String**> | Display name of your connected account. | [optional]
**username** | Option<**String**> | Username of your connected account. | [optional]
**picture** | Option<**String**> | Profile picture of your connected account. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


