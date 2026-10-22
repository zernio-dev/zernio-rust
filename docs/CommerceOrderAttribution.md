# CommerceOrderAttribution

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ready** | Option<**bool**> | False while Shopify is still attributing a new order. No webhook fires when it becomes true, so read the order again later. Always true on WooCommerce. | [optional]
**first_visit** | Option<[**models::CommerceOrderVisit**](CommerceOrderVisit.md)> |  | [optional]
**last_visit** | Option<[**models::CommerceOrderVisit**](CommerceOrderVisit.md)> |  | [optional]
**custom_attributes** | Option<[**Vec<models::BoostPostRequestTrackingUrlTagsInner>**](BoostPostRequestTrackingUrlTagsInner.md)> | Shopify cart and note attributes, or WooCommerce public order meta. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


