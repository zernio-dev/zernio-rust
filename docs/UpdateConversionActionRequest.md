# UpdateConversionActionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (Google Ads) | 
**ad_account_id** | Option<**String**> | Google customer id. Required when the connection has multiple customers. | [optional]
**customer_id** | Option<**String**> | Alias of adAccountId | [optional]
**name** | Option<**String**> |  | [optional]
**status** | Option<**Status**> | REMOVED removes the action and must be sent alone; ENABLED restores a removed one. (enum: ENABLED, REMOVED) | [optional]
**default_value** | Option<**f64**> |  | [optional]
**always_use_default_value** | Option<**bool**> |  | [optional]
**category** | Option<**Category**> | conversion_action.category. Defaults to DEFAULT on create. (enum: DEFAULT, PAGE_VIEW, PURCHASE, SIGNUP, DOWNLOAD, ADD_TO_CART, BEGIN_CHECKOUT, SUBSCRIBE_PAID, PHONE_CALL_LEAD, IMPORTED_LEAD, SUBMIT_LEAD_FORM, BOOK_APPOINTMENT, REQUEST_QUOTE, GET_DIRECTIONS, OUTBOUND_CLICK, CONTACT, ENGAGEMENT, STORE_VISIT, STORE_SALE, QUALIFIED_LEAD, CONVERTED_LEAD) | [optional]
**counting_type** | Option<**CountingType**> | ONE_PER_CLICK counts one conversion per ad click (leads); MANY_PER_CLICK counts every one (purchases). (enum: ONE_PER_CLICK, MANY_PER_CLICK) | [optional]
**default_currency** | Option<**String**> | ISO 4217 currency of defaultValue (value_settings.default_currency_code). | [optional]
**click_through_lookback_window_days** | Option<**i32**> | Days after an ad click a conversion still counts. | [optional]
**view_through_lookback_window_days** | Option<**i32**> | Days after an ad view a view-through conversion still counts. | [optional]
**primary_for_goal** | Option<**bool**> | true = primary (counts toward bidding when its goal is biddable), false = secondary. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


