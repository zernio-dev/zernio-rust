# ListAdAudiences200ResponseAudiencesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | The Zernio audience id. Pass this as audienceId on GET /v1/ads/audiences/{audienceId} and the companies/users upload endpoints. Null when the audience was not created through Zernio. | [optional]
**account_id** | Option<**String**> | Account the audience was created against. Returned for saved_targeting items. | [optional]
**platform_audience_id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**description** | Option<**String**> |  | [optional]
**r#type** | Option<**Type**> |  (enum: customer_list, company_list, engagement, meta_engagement, website, website_retargeting, lookalike, saved_targeting) | [optional]
**spec** | Option<[**models::TargetingSpec**](TargetingSpec.md)> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**size** | Option<**i32**> |  | [optional]
**status** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


