# MetaPromotion

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** | Promotion type accepted by Meta. PERCENTAGE_OFF values cannot exceed 100. (enum: AMOUNT_OFF, FREE_RETURN, FREE_SHIPPING, PERCENTAGE_OFF, PROMO_CODE) | 
**value** | **f64** | Nonnegative promotion value passed to Meta unchanged. AMOUNT_OFF units are not confirmed, including major versus minor currency units. For PERCENTAGE_OFF this is the percentage discount, at most 100. | 
**code** | Option<**String**> | Optional promotion code. | [optional]
**start_date** | Option<**String**> | Optional ISO 8601 start timestamp with a timezone offset or Z. | [optional]
**end_date** | Option<**String**> | Optional ISO 8601 end timestamp with a timezone offset or Z. Must be after startDate when both are set. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


