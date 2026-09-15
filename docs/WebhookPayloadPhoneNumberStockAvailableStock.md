# WebhookPayloadPhoneNumberStockAvailableStock

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**country** | **String** | ISO 3166-1 alpha-2 country code of the watched country. | 
**types** | [**Vec<models::WebhookPayloadPhoneNumberStockAvailableStockTypesInner>**](WebhookPayloadPhoneNumberStockAvailableStockTypesInner.md) | Number types deliverable at sweep time. Only types with stock are listed. | 
**area_code** | Option<**String**> | Set when the watch named an area: the area code (NDC) that is back in stock. | [optional]
**area_name** | Option<**String**> | The name of that area, when known. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


