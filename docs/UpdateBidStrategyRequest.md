# UpdateBidStrategyRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Google ads SocialAccount id. | 
**ad_account_id** | Option<**String**> | Platform ad account ID (Google customer ID, digits only). Defaults to the account's connected customer. | [optional]
**customer_id** | Option<**String**> | Alias of adAccountId, kept for existing callers | [optional]
**name** | Option<**String**> |  | [optional]
**r#type** | Option<**Type**> |  (enum: TARGET_CPA, TARGET_ROAS, MAXIMIZE_CONVERSIONS, MAXIMIZE_CONVERSION_VALUE) | [optional]
**target_cpa** | Option<**f64**> |  | [optional]
**target_roas** | Option<**f64**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


