# CreateAdAudienceRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**ad_account_id** | **String** | Must start with act_ | 
**name** | **String** |  | 
**description** | Option<**String**> |  | [optional]
**r#type** | **Type** |  (enum: customer_list, website, lookalike) | 
**pixel_id** | Option<**String**> | Required for website audiences | [optional]
**retention_days** | Option<**i32**> | Required for website audiences | [optional]
**source_audience_id** | Option<**String**> | Required for lookalike audiences | [optional]
**country** | Option<**String**> | 2-letter code, required for lookalike audiences | [optional]
**ratio** | Option<**f64**> | Required for lookalike audiences | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


