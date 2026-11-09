# ResyncPageWebhookSubscription200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resubscribed** | Option<**bool**> |  | [optional]
**page_id** | Option<**String**> |  | [optional]
**app_subscribed** | Option<**bool**> |  | [optional]
**leadgen** | Option<**bool**> |  | [optional]
**subscribed_fields** | Option<**Vec<String>**> |  | [optional]
**warning** | Option<**String**> |  | [optional]
**instagram_user_id** | Option<**String**> | Instagram accounts only. | [optional]
**subscription_id** | Option<**String**> | Instagram accounts only. Id of the subscription record after the repair. | [optional]
**previous_subscription_id** | Option<**String**> | Instagram accounts only. Id of the record before the repair; null when there was none. | [optional]
**recreated** | Option<**bool**> | Instagram accounts only. True when the subscription record id changed. | [optional]
**missing_fields** | Option<**Vec<String>**> | Instagram accounts only. Webhook fields Zernio expects that Meta did not subscribe. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


