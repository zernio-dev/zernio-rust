# WebhookPayloadAdRuleTriggeredRun

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | ID of the rule run that triggered. | 
**ran_at** | **String** | Scheduled time of the run (UTC). | 
**today** | [**String**](String.md) | The ad account's calendar date (YYYY-MM-DD) the condition windows were resolved against, so `today` and `last_7d` mean the account's days, not UTC days. | 
**timezone** | **String** | IANA timezone used for `today`, for example `Europe/Madrid`. | 
**timezone_assumed** | **bool** | True when the ad account has no known timezone and UTC was assumed. | 
**currency** | Option<**String**> | ISO 4217 currency of the ad account, which money metrics (`spend`, `cpc`, `cpm`, `cpa`) and condition values are in. Null when unknown. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


