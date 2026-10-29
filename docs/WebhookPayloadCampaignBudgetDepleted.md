# WebhookPayloadCampaignBudgetDepleted

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. | 
**profiles** | Option<[**Vec<models::WebhookProfilesInner>**](WebhookProfilesInner.md)> | The profiles this event belongs to, each with the externalId you set on it (null when none is set). Use it to route the event to your tenant without storing Zernio profile ids.  Present on every event tied to a profile, absent on events that belong to none. Events spanning several profiles (a post published to accounts of different profiles) list each once.  | [optional]
**test** | Option<**bool**> | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional]
**event** | **Event** |  (enum: campaign.budget.depleted) | 
**account** | [**models::WebhookAdsAccount**](WebhookAdsAccount.md) |  | 
**ad_object** | [**models::WebhookPayloadCampaignBudgetDepletedAdObject**](WebhookPayloadCampaignBudgetDepletedAdObject.md) |  | 
**budget** | [**models::WebhookPayloadCampaignBudgetDepletedBudget**](WebhookPayloadCampaignBudgetDepletedBudget.md) |  | 
**timestamp** | **String** | UTC time at which Zernio generated this event. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


