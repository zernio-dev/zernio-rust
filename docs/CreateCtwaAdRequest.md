# CreateCtwaAdRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Facebook or Instagram SocialAccount ID. | 
**ad_account_id** | **String** | Meta ad account ID, e.g. `act_123456789`. | 
**name** | **String** | Ad display name. Used to derive campaign / ad set names. | 
**headline** | **String** |  | 
**body** | **String** | Primary text shown above the image / video. | 
**image_url** | Option<**String**> | Image asset for image creatives. Mutually exclusive with `video`. Required if `video` is not supplied.  | [optional]
**video** | Option<[**models::CreateCtwaAdRequestVideo**](CreateCtwaAdRequestVideo.md)> |  | [optional]
**budget_amount** | **f64** | Budget amount in the ad account's currency major units (e.g. dollars for USD, not cents). Must be > 0.  | 
**budget_type** | **BudgetType** |  (enum: daily, lifetime) | 
**currency** | Option<**String**> | ISO 4217 currency code matching the ad account's currency (e.g. `USD`). Optional; Meta infers from the ad account when omitted.  | [optional]
**end_date** | Option<**String**> | ISO 8601 datetime. Required when `budgetType` is `lifetime`.  | [optional]
**countries** | Option<**Vec<String>**> | ISO 3166-1 alpha-2 country codes. Defaults to `[\"US\"]`. | [optional]
**age_min** | Option<**i32**> |  | [optional]
**age_max** | Option<**i32**> |  | [optional]
**interests** | Option<[**Vec<models::CreateCtwaAdRequestInterestsInner>**](CreateCtwaAdRequestInterestsInner.md)> |  | [optional]
**audience_id** | Option<**String**> | Custom audience ID to target. | [optional]
**advantage_audience** | Option<**AdvantageAudience**> | Meta's Advantage+ audience expansion. `0` (default) keeps targeting strict; `1` lets Meta expand beyond the supplied targeting when its delivery system finds better matches. Always sent on CREATE (Meta requires it).  (enum: 0, 1) | [optional]
**objective** | Option<**Objective**> | Defaults to `OUTCOME_ENGAGEMENT` (the broadly-supported CTWA objective). `OUTCOME_SALES` and `OUTCOME_LEADS` require additional account configuration (Dataset linked to the WABA for sales) and may be rejected by Meta if missing.  (enum: OUTCOME_ENGAGEMENT, OUTCOME_SALES, OUTCOME_LEADS) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


