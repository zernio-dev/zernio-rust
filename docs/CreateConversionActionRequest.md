# CreateConversionActionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | SocialAccount ID. Must be a `googleads` account. | 
**ad_account_id** | Option<**String**> | Platform ad account ID (Google customer ID, digits only). Resolved automatically when the connection has exactly one accessible customer. | [optional]
**customer_id** | Option<**String**> | Alias of adAccountId, kept for existing callers | [optional]
**name** | **String** |  | 
**r#type** | **Type** | Only WEBPAGE is supported for creation today. (enum: WEBPAGE) | 
**default_value** | Option<**f64**> | Default conversion value used when an event doesn't carry its own value. | [optional]
**always_use_default_value** | Option<**bool**> | When true, always use defaultValue and ignore any value sent with the event. Defaults to true when defaultValue is set. | [optional]
**category** | Option<**Category**> | conversion_action.category. Defaults to DEFAULT on create. (enum: DEFAULT, PAGE_VIEW, PURCHASE, SIGNUP, DOWNLOAD, ADD_TO_CART, BEGIN_CHECKOUT, SUBSCRIBE_PAID, PHONE_CALL_LEAD, IMPORTED_LEAD, SUBMIT_LEAD_FORM, BOOK_APPOINTMENT, REQUEST_QUOTE, GET_DIRECTIONS, OUTBOUND_CLICK, CONTACT, ENGAGEMENT, STORE_VISIT, STORE_SALE, QUALIFIED_LEAD, CONVERTED_LEAD) | [optional]
**counting_type** | Option<**CountingType**> | ONE_PER_CLICK counts one conversion per ad click (leads); MANY_PER_CLICK counts every one (purchases). (enum: ONE_PER_CLICK, MANY_PER_CLICK) | [optional]
**default_currency** | Option<**String**> | ISO 4217 currency of defaultValue (value_settings.default_currency_code). | [optional]
**click_through_lookback_window_days** | Option<**i32**> | Days after an ad click a conversion still counts. | [optional]
**view_through_lookback_window_days** | Option<**i32**> | Days after an ad view a view-through conversion still counts. | [optional]
**primary_for_goal** | Option<**bool**> | true = primary (counts toward bidding when its goal is biddable), false = secondary. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


