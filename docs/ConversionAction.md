# ConversionAction

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Google Ads conversion action id. | 
**name** | **String** |  | 
**r#type** | **String** | Google's ConversionActionType, e.g. WEBPAGE, UPLOAD_CLICKS. | 
**status** | **String** | Google's ConversionActionStatus, e.g. ENABLED, REMOVED, HIDDEN. | 
**category** | **String** | Google's ConversionActionCategory, e.g. DEFAULT, PURCHASE, LEAD. | 
**origin** | Option<**String**> | Google's ConversionOrigin, e.g. WEBSITE, APP. Together with category it names the goal the action belongs to (see GET /v1/ads/conversions/goals). | [optional]
**primary_for_goal** | Option<**bool**> | true = primary (counts toward bidding when its goal is biddable), false = secondary. Change it with PATCH /v1/ads/conversions/actions/{actionId}. | [optional]
**default_value** | Option<**f64**> | Value recorded when the conversion carries none. | [optional]
**default_currency** | Option<**String**> | ISO 4217 currency of defaultValue. | [optional]
**always_use_default_value** | Option<**bool**> | true = defaultValue is used even when the conversion sends its own value. | [optional]
**counting_type** | Option<**String**> | Google's ConversionActionCountingType: ONE_PER_CLICK or MANY_PER_CLICK. | [optional]
**click_through_lookback_window_days** | Option<**i32**> | Days after an ad click a conversion is still credited (1 to 90). | [optional]
**view_through_lookback_window_days** | Option<**i32**> | Days after an ad view a conversion is still credited (1 to 30). | [optional]
**tag_snippets** | [**Vec<models::ConversionActionTagSnippetsInner>**](ConversionActionTagSnippetsInner.md) | The code a customer pastes onto their site. Present for types Google generates a snippet for (e.g. WEBPAGE); empty otherwise.  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


