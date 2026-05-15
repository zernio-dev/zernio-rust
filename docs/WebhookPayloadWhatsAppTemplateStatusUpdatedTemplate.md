# WebhookPayloadWhatsAppTemplateStatusUpdatedTemplate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**template_id** | **String** | Meta's `message_template_id`, returned as a string. | 
**name** | **String** | Meta's `message_template_name`. | 
**language** | **String** | Meta's `message_template_language` (e.g. `en_US`). | 
**status** | **Status** | New status. Forwarded verbatim from Meta's `event` field. `PENDING_DELETION` is the 24h-grace state after a delete request before the template is actually removed.  (enum: APPROVED, REJECTED, PENDING, PAUSED, DISABLED, IN_APPEAL, PENDING_DELETION) | 
**reason** | **String** | Meta's free-form reason for the transition. `\"NONE\"` on approval; an explanation string on rejection.  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


