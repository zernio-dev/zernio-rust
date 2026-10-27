# CreateStandaloneAd201ResponseOneOf1

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ads** | Option<[**Vec<models::Ad>**](Ad.md)> |  | [optional]
**platform_campaign_id** | Option<**String**> |  | [optional]
**platform_ad_set_id** | Option<**String**> |  | [optional]
**applied_defaults** | Option<[**models::AdAppliedDefaults**](AdAppliedDefaults.md)> |  | [optional]
**message** | Option<**String**> |  | [optional]
**warnings** | Option<**Vec<String>**> | Meta only, present only when needed. An `activation_failed:` entry means Meta refused the final switch to ACTIVE for the ads it names (or for their ad set or campaign): the entry names what was kept PAUSED and what was switched ACTIVE, and quotes Meta's error and the status calls that switch the PAUSED ones on later. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


