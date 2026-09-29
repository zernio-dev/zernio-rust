# CommerceCollection

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Platform-native collection id. | [optional]
**account_id** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: shopify, woocommerce) | [optional]
**title** | Option<**String**> |  | [optional]
**handle** | Option<**String**> |  | [optional]
**description_html** | Option<**String**> |  | [optional]
**image** | Option<[**models::CommerceImage**](CommerceImage.md)> |  | [optional]
**sort_order** | Option<**SortOrder**> |  (enum: manual, best_selling, alpha_asc, alpha_desc, price_asc, price_desc, created, created_desc, most_relevant) | [optional]
**product_count** | Option<**i32**> | Updates a few seconds after a membership change. | [optional]
**seo** | Option<[**models::ProductSeo**](ProductSeo.md)> |  | [optional]
**updated_at** | Option<**String**> |  | [optional]
**platform_data** | Option<**std::collections::HashMap<String, serde_json::Value>**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


