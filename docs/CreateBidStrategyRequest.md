# CreateBidStrategyRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Google ads SocialAccount id. | 
**ad_account_id** | Option<**String**> | Platform ad account ID (Google customer ID, digits only). Defaults to the account's connected customer. | [optional]
**customer_id** | Option<**String**> | Alias of adAccountId, kept for existing callers | [optional]
**name** | **String** |  | 
**r#type** | **Type** |  (enum: TARGET_CPA, TARGET_ROAS, MAXIMIZE_CONVERSIONS, MAXIMIZE_CONVERSION_VALUE) | 
**target_cpa** | Option<**f64**> | Required when type is TARGET_CPA, in the account's currency units. | [optional]
**target_roas** | Option<**f64**> | Required when type is TARGET_ROAS; a multiplier (2.0 = 2.0x). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


