# CustomConversionResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_account_id** | Option<**String**> |  | [optional]
**custom_conversion_id** | Option<**String**> | Drops straight into promotedObject.customConversionId on POST /v1/ads/create. | [optional]
**reused** | Option<**bool**> | True when an existing conversion matched name + pixelId; the response is then a 200. | [optional]
**custom_conversion** | Option<[**models::CustomConversion**](CustomConversion.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


