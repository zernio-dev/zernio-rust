# GetPageWebhookSubscription200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**page_id** | Option<**String**> |  | [optional]
**app_subscribed** | Option<**bool**> | False when the Page carries no subscription for our app at all. | [optional]
**leadgen** | Option<**bool**> | Whether lead ads submitted on this Page reach Zernio in real time. | [optional]
**subscribed_fields** | Option<**Vec<String>**> |  | [optional]
**warning** | Option<**String**> | Present only when leadgen is missing. | [optional]
**instagram_user_id** | Option<**String**> | Instagram accounts only. | [optional]
**subscription_id** | Option<**String**> | Instagram accounts only. Id of the subscription record on Meta; null when there is none. | [optional]
**missing_fields** | Option<**Vec<String>**> | Instagram accounts only. Webhook fields Zernio expects that Meta did not subscribe. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


