# WebhookPayloadAdStatusChanged

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Stable webhook event ID | 
**event** | **Event** |  (enum: ad.status_changed) | 
**account** | [**models::WebhookPayloadAdStatusChangedAccount**](WebhookPayloadAdStatusChangedAccount.md) |  | 
**ad_object** | [**models::WebhookPayloadAdStatusChangedAdObject**](WebhookPayloadAdStatusChangedAdObject.md) |  | 
**status** | [**models::WebhookPayloadAdStatusChangedStatus**](WebhookPayloadAdStatusChangedStatus.md) |  | 
**error** | Option<[**models::WebhookPayloadAdStatusChangedError**](WebhookPayloadAdStatusChangedError.md)> |  | [optional]
**timestamp** | **String** | ISO-8601 timestamp the webhook was produced. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


