# GetEvent200ResponseTouchesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**at** | Option<**String**> |  | [optional]
**kind** | Option<**Kind**> |  (enum: ad_click, paid, email, social, campaign, organic_search, ai_assistant, referral, lead_form, event, survey) | [optional]
**platform** | Option<**String**> | The ad platform of the campaign, or the one a survey answer names (Instagram reads as facebook). | [optional]
**ad_account_id** | Option<**String**> |  | [optional]
**campaign_id** | Option<**String**> | The campaign the touch resolved to; null for a touch that named none (search, referral). | [optional]
**credit** | Option<**std::collections::HashMap<String, f64>**> | The share of the event (0 to 1) this touch gets per model: first_touch, last_non_direct, linear, position_based, time_decay, w_shaped. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


