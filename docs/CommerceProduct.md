# CommerceProduct

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Platform-native product id. | [optional]
**account_id** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: shopify) | [optional]
**title** | Option<**String**> |  | [optional]
**description_html** | Option<**String**> |  | [optional]
**handle** | Option<**String**> | URL slug of the product. | [optional]
**vendor** | Option<**String**> |  | [optional]
**product_type** | Option<**String**> |  | [optional]
**tags** | Option<**Vec<String>**> |  | [optional]
**status** | Option<[**models::CommerceProductStatus**](CommerceProductStatus.md)> |  | [optional]
**platform_status** | Option<**String**> | The raw status on the platform, e.g. ACTIVE on Shopify. | [optional]
**featured_image** | Option<[**models::CommerceImage**](CommerceImage.md)> |  | [optional]
**images** | Option<[**Vec<models::CommerceImage>**](CommerceImage.md)> | First 20 images, in store order. | [optional]
**options** | Option<[**Vec<models::ProductOptionsInner>**](ProductOptionsInner.md)> | Option axes (e.g. Size, Color) and their values. | [optional]
**variants** | Option<[**Vec<models::CommerceVariant>**](CommerceVariant.md)> | First 100 variants. | [optional]
**total_inventory** | Option<**i32**> |  | [optional]
**url** | Option<**String**> | Public storefront URL; null while the product is not published. | [optional]
**seo** | Option<[**models::ProductSeo**](ProductSeo.md)> |  | [optional]
**created_at** | Option<**String**> |  | [optional]
**updated_at** | Option<**String**> |  | [optional]
**published_at** | Option<**String**> |  | [optional]
**platform_data** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Platform-only fields. Null when the platform has none. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


