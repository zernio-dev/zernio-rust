# ListAdAudiences200ResponseAudiencesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**platform_audience_id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**description** | Option<**String**> |  | [optional]
**r#type** | Option<**Type**> |  (enum: customer_list, website, lookalike, saved_targeting) | [optional]
**spec** | Option<[**models::TargetingSpec**](TargetingSpec.md)> | Present (and the only meaningful payload) when `type` is `saved_targeting`. Null for uploaded/derived audience types. | [optional]
**platform** | Option<**String**> |  | [optional]
**size** | Option<**i32**> |  | [optional]
**status** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


