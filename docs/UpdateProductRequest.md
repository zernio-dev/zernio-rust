# UpdateProductRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | Option<**String**> |  | [optional]
**description_html** | Option<**String**> | Product description as HTML. | [optional]
**handle** | Option<**String**> | URL slug of the product. | [optional]
**vendor** | Option<**String**> |  | [optional]
**product_type** | Option<**String**> |  | [optional]
**tags** | Option<**Vec<String>**> | Replaces the full tag list. | [optional]
**status** | Option<**Status**> | archived hides the product everywhere; draft keeps it editable but unpublished. (enum: active, draft, archived) | [optional]
**seo** | Option<[**models::UpdateProductRequestSeo**](UpdateProductRequestSeo.md)> |  | [optional]
**variants** | Option<[**Vec<models::UpdateProductRequestVariantsInner>**](UpdateProductRequestVariantsInner.md)> | Price changes per variant. Only the listed variants change. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


