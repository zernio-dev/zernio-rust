# EstimateAdReachRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio account ID on the target ad platform (the estimate runs against its platform). | 
**ad_account_id** | **String** | Required. The platform ad-account ID the reach call runs against (Meta act_..., LinkedIn numeric sponsoredAccount ID, Pinterest ad-account ID, X account ID) - every backing reach API is scoped to one ad account. Get it from GET /v1/ads/accounts. | 
**spec** | Option<[**models::TargetingSpec**](TargetingSpec.md)> | The targeting spec to estimate. Same shape used by POST /v1/ads/create. Required unless `rawTargeting` is sent; with `rawTargeting` it can be omitted or minimal. | [optional]
**raw_targeting** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Meta only. A Meta-native targeting spec (snake_case: `geo_locations`, `age_min`, `flexible_spec`, `excluded_custom_audiences`, `user_os`, ...), the same field `POST /v1/ads/create` accepts, so the estimate covers the exact audience the ad set will use. Sending it for an account on another platform returns 400 naming `rawTargeting`.  For layered targeting, send `flexible_spec` here: entries AND together, ids inside one entry OR.  **Merge rules** (same as `POST /v1/ads/create`):  - rawTargeting is the BASE layer; `spec`, converted to Meta's wire shape, is merged on top key by key, with `spec` winning on collision. - The merge goes one level deep inside `geo_locations` and `excluded_geo_locations` (spec sub-keys win, raw-only sub-keys such as `location_types` survive). - Array values (`flexible_spec`, ...) are replaced as a whole key when `spec` builds them, never element-merged, so `spec.interests` or `spec.behaviors` replace a raw `flexible_spec`.  The result is sent to Meta `delivery_estimate` as `targeting_spec`.  | [optional]
**optimization_goal** | Option<**String**> | Optional. The optimization goal the estimate should assume (platform's own vocabulary, e.g. Meta `REACH`, `LINK_CLICKS`, `OFFSITE_CONVERSIONS`). Some platforms vary the estimate by goal; omit to use the platform default.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


