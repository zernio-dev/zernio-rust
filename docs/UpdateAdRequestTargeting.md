# UpdateAdRequestTargeting

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**keywords** | Option<[**Vec<models::UpdateAdRequestTargetingKeywordsInner>**](UpdateAdRequestTargetingKeywordsInner.md)> | Google only. The FULL desired set of positive keywords for the entire ad group. Omit to leave positives unchanged; [] removes all positives. Negatives are independent. Entries are strings (BROAD) or { text, matchType } with matchType exact | phrase | broad; an omitted matchType also defaults to BROAD. Matching case-insensitive text AND match type retains the existing criterion ID, status, bid overrides, labels and history without a mutation. A changed text or match type uses remove/create, without transferring the old criterion's attributes or history. See Google keyword replacement above for an EXACT-to-BROAD example. Mirrored to GET /v1/ads/keywords immediately.  | [optional]
**negative_keywords** | Option<[**Vec<models::UpdateAdRequestTargetingKeywordsInner>**](UpdateAdRequestTargetingKeywordsInner.md)> | Google only. The FULL desired set of negative keywords for the entire ad group, independent of positives. Omit to leave negatives unchanged; [] removes all negatives. Uses the same text/match-type identity and preservation contract as keywords above. Strings and objects without matchType default to BROAD, so resending an EXACT or PHRASE negative as a bare string requests a different criterion. Campaign negatives are separate: use /v1/ads/campaigns/{campaignId}/negative-keywords to manage those.  | [optional]
**devices** | Option<[**Vec<models::UpdateAdRequestTargetingDevicesInner>**](UpdateAdRequestTargetingDevicesInner.md)> | Google only. The FULL new set of device criteria for the campaign; devices not listed are excluded. Entries are a device name alone (included, no bid adjustment) or { device, bidModifier }. | [optional]
**age_min** | Option<**i32**> |  | [optional]
**age_max** | Option<**i32**> |  | [optional]
**countries** | Option<**Vec<String>**> |  | [optional]
**interests** | Option<[**Vec<models::UpdateAdRequestTargetingInterestsInner>**](UpdateAdRequestTargetingInterestsInner.md)> | Interest objects from /v1/ads/interests. Each must include id and name. | [optional]
**advantage_audience** | Option<**AdvantageAudience**> | Meta only. Omit to preserve the existing setting on update. 0 = disabled, 1 = enabled. (enum: 0, 1) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


