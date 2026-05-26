# CreateInboxConversationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | The social account ID to send from | 
**participant_id** | Option<**String**> | Recipient identifier. For X this is the numeric user ID; for WhatsApp, the recipient phone number in international format (digits, country code included). Provide either this or participantUsername. | [optional]
**participant_username** | Option<**String**> | Recipient handle/username — an X or Bluesky handle (with or without @) or a Reddit username (with or without u/). Resolved via lookup. Provide either this or participantId. | [optional]
**message** | Option<**String**> | Text content of the message. At least one of message, attachment, or (for WhatsApp) templateName is required. | [optional]
**skip_dm_check** | Option<**bool**> | X/Twitter only. Skip the receives_your_dm eligibility check before sending. Use if you have already verified the recipient accepts DMs. | [optional][default to false]
**template_name** | Option<**String**> | WhatsApp only. Name of the approved template to start the conversation with (required for WhatsApp). | [optional]
**template_language** | Option<**String**> | WhatsApp only. Template language code (e.g. en_US). | [optional]
**template_params** | Option<**Vec<String>**> | WhatsApp only. Body variable values, in order, substituted into the template body ({{1}}, {{2}}, ...). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


