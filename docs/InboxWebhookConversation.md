# InboxWebhookConversation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Zernio's internal conversation id (also the message's conversationId). Accepted by every /v1/inbox/conversations/{conversationId} endpoint. | 
**platform_conversation_id** | **String** | The platform's conversation id. This is the `id` GET /v1/inbox/conversations returns for the same conversation (on Instagram and Messenger it is the participant's IGSID / PSID), so key your records on it to match webhooks with list rows. Also accepted by the conversation endpoints. | 
**participant_id** | Option<**String**> |  | [optional]
**participant_name** | Option<**String**> |  | [optional]
**participant_username** | Option<**String**> |  | [optional]
**participant_picture** | Option<**String**> |  | [optional]
**status** | **Status** |  (enum: active, archived) | 
**contact_id** | Option<**String**> | Zernio CRM Contact ID for the participant, when one exists. Resolved by joining `participantId` to the ContactChannel collection. Best-effort: omitted when no channel matches or `participantId` is absent. Lets integrators join any inbox webhook back to the CRM Contact without needing to look at the sender, which matters for outgoing and delivery-status events whose sender is the business.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


