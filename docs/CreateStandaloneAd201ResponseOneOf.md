# CreateStandaloneAd201ResponseOneOf

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad** | Option<[**models::Ad**](Ad.md)> |  | [optional]
**applied_defaults** | Option<[**models::AdAppliedDefaults**](AdAppliedDefaults.md)> |  | [optional]
**message** | Option<**String**> |  | [optional]
**warnings** | Option<**Vec<String>**> | Meta only, present only when needed. An `activation_failed:` entry means Meta refused the final switch to ACTIVE: the entry names what was kept PAUSED (the ad, and its ad set or campaign when Meta refused those) and what was switched ACTIVE, and quotes Meta's error and the status calls that switch the PAUSED ones on later. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


