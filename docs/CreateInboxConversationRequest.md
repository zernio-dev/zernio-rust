# CreateInboxConversationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | The social account ID to send from | 
**participant_id** | Option<**String**> | Twitter numeric user ID of the recipient. Provide either this or participantUsername. | [optional]
**participant_username** | Option<**String**> | Twitter username (with or without @) of the recipient. Resolved to a user ID via lookup. Provide either this or participantId. | [optional]
**message** | Option<**String**> | Text content of the message. At least one of message or attachment is required. | [optional]
**skip_dm_check** | Option<**bool**> | Skip the receives_your_dm eligibility check before sending. Use if you have already verified the recipient accepts DMs. | [optional][default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


