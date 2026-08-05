# ValueRuleCriterion

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Platform criterion id. Echo it on `PUT` to KEEP this criterion, omit it to CREATE a new one. A criterion left out of the array entirely is DELETED.  | [optional]
**criteria_type** | **CriteriaType** | The dimension being matched. `OMNI_CHANNEL` (conversion location: APP, INSTANT_FORM, PHONE_CALL, WEBSITE) is accepted even though Meta's own enum table omits it.  (enum: AGE, GENDER, OS_TYPE, DEVICE_PLATFORM, LOCATION, PLACEMENT, OMNI_CHANNEL, AUDIENCE_LABEL) | 
**operator** | **Operator** | Required on every criterion. `CONTAINS` is currently the only value Meta supports. (enum: CONTAINS) | 
**criteria_values** | **Vec<String>** | The values to match. `AGE` takes ranges such as `18-24`, `18+` or a custom `18-26`; a range whose upper bound is 65 is NOT allowed (use `18+` instead of `18-65`). `LOCATION` takes Targeting-Search keys: a two-letter country code for `LOCATION_COUNTRY`, a numeric key for region / city / comScore market. `AUDIENCE_LABEL` takes labels such as `HIGH_VALUE`, which are applied to a Custom Audience in Ads Manager: there is no API to provision them, so they are passed through unvalidated.  | 
**criteria_value_types** | **Vec<String>** | One entry per `criteriaValues` entry, in the same order. The literal `\"NONE\"` for every criteriaType except `LOCATION`, which uses `LOCATION_COUNTRY`, `LOCATION_REGION`, `LOCATION_CITY` or `LOCATION_COMSCORE_MARKET` and MAY mix them within one criterion. `LOCATION_DMA` was replaced by `LOCATION_COMSCORE_MARKET` on 2026-06-22 and is rejected by this API.  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


