# Product

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Platform-native product id (numeric string for Shopify). | [optional]
**platform** | Option<**Platform**> |  (enum: shopify) | [optional]
**title** | Option<**String**> |  | [optional]
**handle** | Option<**String**> | URL slug of the product. | [optional]
**description_html** | Option<**String**> | Product description as HTML. | [optional]
**vendor** | Option<**String**> |  | [optional]
**product_type** | Option<**String**> | Free-text product type as set on the store. | [optional]
**tags** | Option<**Vec<String>**> |  | [optional]
**status** | Option<**Status**> |  (enum: active, draft, archived) | [optional]
**featured_image** | Option<[**models::ProductImage**](ProductImage.md)> |  | [optional]
**images** | Option<[**Vec<models::ProductImage>**](ProductImage.md)> | First 20 images in the product media, in store order. | [optional]
**options** | Option<[**Vec<models::ProductOptionsInner>**](ProductOptionsInner.md)> | Option axes (e.g. Size, Color) and their values. | [optional]
**variants** | Option<[**Vec<models::ProductVariant>**](ProductVariant.md)> | First 100 variants. | [optional]
**seo** | Option<[**models::ProductSeo**](ProductSeo.md)> |  | [optional]
**total_inventory** | Option<**i32**> |  | [optional]
**online_store_url** | Option<**String**> | Public storefront URL; null while the product is not published to the online store. | [optional]
**created_at** | Option<**String**> |  | [optional]
**updated_at** | Option<**String**> |  | [optional]
**published_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


