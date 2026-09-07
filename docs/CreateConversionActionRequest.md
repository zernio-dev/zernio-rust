# CreateConversionActionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | SocialAccount ID. Must be a `googleads` account. | 
**customer_id** | Option<**String**> | Google Ads customer id (digits only). Resolved automatically when the connection has exactly one accessible customer. | [optional]
**name** | **String** |  | 
**r#type** | **Type** | Only WEBPAGE is supported for creation today. (enum: WEBPAGE) | 
**default_value** | Option<**f64**> | Default conversion value used when an event doesn't carry its own value. | [optional]
**always_use_default_value** | Option<**bool**> | When true, always use defaultValue and ignore any value sent with the event. Defaults to true when defaultValue is set. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


