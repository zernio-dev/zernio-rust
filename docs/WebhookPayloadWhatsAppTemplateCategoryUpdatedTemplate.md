# WebhookPayloadWhatsAppTemplateCategoryUpdatedTemplate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**template_id** | **String** | Meta's `message_template_id`, returned as a string. | 
**name** | **String** | Meta's `message_template_name`. | 
**language** | **String** | Meta's `message_template_language` (e.g. `en_US`). | 
**change_type** | **ChangeType** | `scheduled` is Meta's 24h advance notice of an upcoming reclassification; `applied` is the change taking effect.  (enum: scheduled, applied) | 
**category** | **Category** | The category right now, regardless of changeType. (enum: UTILITY, MARKETING, AUTHENTICATION) | 
**previous_category** | Option<**PreviousCategory**> | Present only when changeType is `applied`. The category before this change. (enum: UTILITY, MARKETING, AUTHENTICATION) | [optional]
**scheduled_category** | Option<**ScheduledCategory**> | Present only when changeType is `scheduled`. The category that will take effect at `effectiveAt`. (enum: UTILITY, MARKETING, AUTHENTICATION) | [optional]
**effective_at** | Option<**String**> | Present only when changeType is `scheduled`. ISO-8601 timestamp when the scheduled category takes effect. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


