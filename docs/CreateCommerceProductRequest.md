# CreateCommerceProductRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**title** | **String** |  | 
**description_html** | Option<**String**> |  | [optional]
**handle** | Option<**String**> |  | [optional]
**vendor** | Option<**String**> |  | [optional]
**product_type** | Option<**String**> |  | [optional]
**tags** | Option<**Vec<String>**> |  | [optional]
**seo** | Option<[**models::CreateCommerceProductRequestSeo**](CreateCommerceProductRequestSeo.md)> |  | [optional]
**status** | Option<**Status**> |  (enum: draft, active) | [optional][default to Draft]
**images** | Option<[**Vec<models::CreateCommerceProductRequestImagesInner>**](CreateCommerceProductRequestImagesInner.md)> |  | [optional]
**options** | Option<[**Vec<models::CreateCommerceProductRequestOptionsInner>**](CreateCommerceProductRequestOptionsInner.md)> |  | [optional]
**variants** | [**Vec<models::CreateCommerceProductRequestVariantsInner>**](CreateCommerceProductRequestVariantsInner.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


