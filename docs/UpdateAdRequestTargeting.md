# UpdateAdRequestTargeting

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**keywords** | Option<[**Vec<models::UpdateAdRequestTargetingKeywordsInner>**](UpdateAdRequestTargetingKeywordsInner.md)> | Google only. The FULL new set of positive keywords for the ad group; live keywords not listed are removed. Entries are strings (BROAD) or { text, matchType } with matchType exact | phrase | broad. Mirrored to GET /v1/ads/keywords immediately. | [optional]
**negative_keywords** | Option<[**Vec<models::UpdateAdRequestTargetingKeywordsInner>**](UpdateAdRequestTargetingKeywordsInner.md)> | Google only. Same declarative contract as keywords, for the ad group's negative keywords. | [optional]
**age_min** | Option<**i32**> |  | [optional]
**age_max** | Option<**i32**> |  | [optional]
**countries** | Option<**Vec<String>**> |  | [optional]
**interests** | Option<[**Vec<models::UpdateAdRequestTargetingInterestsInner>**](UpdateAdRequestTargetingInterestsInner.md)> | Interest objects from /v1/ads/interests. Each must include id and name. | [optional]
**advantage_audience** | Option<**AdvantageAudience**> | Meta only. Omit to preserve the existing setting on update. 0 = disabled, 1 = enabled. (enum: 0, 1) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


