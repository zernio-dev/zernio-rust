# UpdateConversionDestinationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_account_id** | **String** |  | 
**name** | Option<**String**> |  | [optional]
**enabled** | Option<**bool**> | Setting `false` is equivalent to calling DELETE — the rule will appear as `inactive` afterwards.  | [optional]
**attribution_type** | Option<**AttributionType**> |  (enum: LAST_TOUCH_BY_CAMPAIGN, LAST_TOUCH_BY_CONVERSION) | [optional]
**post_click_attribution_window_size** | Option<**PostClickAttributionWindowSize**> | 365 only allowed for LEAD, PURCHASE, ADD_TO_CART, QUALIFIED_LEAD, SUBMIT_APPLICATION rule types.  (enum: 1, 7, 30, 90, 365) | [optional]
**view_through_attribution_window_size** | Option<**ViewThroughAttributionWindowSize**> | 365 only allowed for LEAD, PURCHASE, ADD_TO_CART, QUALIFIED_LEAD, SUBMIT_APPLICATION rule types.  (enum: 1, 7, 30, 90, 365) | [optional]
**value_type** | Option<**ValueType**> |  (enum: DYNAMIC, FIXED, NO_VALUE) | [optional]
**value** | Option<[**models::UpdateConversionDestinationRequestValue**](UpdateConversionDestinationRequestValue.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


