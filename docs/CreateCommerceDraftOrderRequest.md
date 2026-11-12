# CreateCommerceDraftOrderRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Connected store SocialAccount id. | 
**customer_id** | Option<**String**> | The customer it is for, from the customers endpoints. | [optional]
**email** | Option<**String**> |  | [optional]
**line_items** | [**Vec<models::CreateCommerceDraftOrderRequestLineItemsInner>**](CreateCommerceDraftOrderRequestLineItemsInner.md) | A product variant (variantId) or a custom item (title and price). | 
**discount** | Option<[**models::CreateCommerceDraftOrderRequestDiscount**](CreateCommerceDraftOrderRequestDiscount.md)> |  | [optional]
**shipping** | Option<[**models::CreateCommerceDraftOrderRequestShipping**](CreateCommerceDraftOrderRequestShipping.md)> |  | [optional]
**shipping_address** | Option<[**models::CreateCommerceDraftOrderRequestShippingAddress**](CreateCommerceDraftOrderRequestShippingAddress.md)> |  | [optional]
**note** | Option<**String**> |  | [optional]
**tags** | Option<**Vec<String>**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


