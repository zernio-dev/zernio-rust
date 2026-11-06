# AutomationTemplateInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **String** | The name to send the value under in `inputs`, for example `adAccount`. | 
**r#type** | **Type** | What the value is. `ad_account`: `{ accountId, adAccountId }`. `profile`: a profile id. `social_accounts`: an array of social account ids. `notify_destination`: an array of `{ accountId, to?, channelId? }`. `number`, `money` (in the ad account's currency) and `percent`: a number within the bounds below. `choice`: one of `options[].value`. (enum: ad_account, profile, social_accounts, notify_destination, number, money, percent, choice) | 
**label** | **String** |  | 
**optional** | Option<**bool**> | True when an install may leave it out. A field that points at a left-out input is dropped. | [optional]
**default** | Option<[**models::AutomationTemplateInputDefault**](AutomationTemplateInputDefault.md)> |  | [optional]
**min** | Option<**f64**> |  | [optional]
**exclusive_min** | Option<**f64**> | The value must be above it, for example an amount above 0. | [optional]
**max** | Option<**f64**> |  | [optional]
**integer** | Option<**bool**> | True when only whole numbers are accepted. | [optional]
**options** | Option<[**Vec<models::AutomationTemplateInputOptionsInner>**](AutomationTemplateInputOptionsInner.md)> | What a `choice` input offers. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


