# CreateCommerceCollectionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**title** | **String** |  | 
**description_html** | Option<**String**> |  | [optional]
**handle** | Option<**String**> |  | [optional]
**sort_order** | Option<**SortOrder**> |  (enum: manual, best_selling, alpha_asc, alpha_desc, price_asc, price_desc, created, created_desc, most_relevant) | [optional]
**seo** | Option<[**models::CreateCommerceProductRequestSeo**](CreateCommerceProductRequestSeo.md)> |  | [optional]
**image** | Option<[**models::CreateCommerceProductRequestImagesInner**](CreateCommerceProductRequestImagesInner.md)> |  | [optional]
**product_ids** | Option<**Vec<String>**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


