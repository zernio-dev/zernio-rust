# WebhookPayloadAdRuleTriggeredObjectsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform_id** | **String** | Platform-native ID of the campaign or ad set. | 
**name** | **String** | Name on the platform. Falls back to `platformId` when the platform reports none. | 
**platform_campaign_id** | Option<**String**> | Platform-native ID of the campaign the object belongs to (on a campaign-level rule, the campaign's own ID). Null when unknown. | 
**conditions** | [**Vec<models::WebhookPayloadAdRuleTriggeredObjectsInnerConditionsInner>**](WebhookPayloadAdRuleTriggeredObjectsInnerConditionsInner.md) | Every condition of the rule, with the value the object reached. | 
**actions** | [**Vec<models::WebhookPayloadAdRuleTriggeredObjectsInnerActionsInner>**](WebhookPayloadAdRuleTriggeredObjectsInnerActionsInner.md) | What the rule did to the object. Empty on a rule that only notifies. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


