# CommerceDiscount

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: shopify) | [optional]
**title** | Option<**String**> |  | [optional]
**method** | Option<**Method**> |  (enum: code, automatic) | [optional]
**r#type** | Option<**Type**> |  (enum: percentage, fixed_amount, free_shipping, buy_x_get_y, app) | [optional]
**codes** | Option<**Vec<String>**> | The first 10 codes; codeCount has the total. | [optional]
**code_count** | Option<**i32**> |  | [optional]
**value** | Option<[**models::CommerceDiscountValue**](CommerceDiscountValue.md)> |  | [optional]
**applies_to** | Option<[**models::CommerceDiscountAppliesTo**](CommerceDiscountAppliesTo.md)> |  | [optional]
**minimum** | Option<[**models::CommerceDiscountMinimum**](CommerceDiscountMinimum.md)> |  | [optional]
**usage_limit** | Option<**i32**> |  | [optional]
**once_per_customer** | Option<**bool**> |  | [optional]
**usage_count** | Option<**i32**> |  | [optional]
**starts_at** | Option<**String**> |  | [optional]
**ends_at** | Option<**String**> |  | [optional]
**status** | Option<**Status**> |  (enum: active, scheduled, expired) | [optional]
**platform_status** | Option<**String**> |  | [optional]
**summary** | Option<**String**> |  | [optional]
**platform_data** | Option<**std::collections::HashMap<String, serde_json::Value>**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


