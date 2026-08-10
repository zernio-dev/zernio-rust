# GetAdsSearchTerms200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**search_term** | Option<**String**> |  | [optional]
**status** | Option<**String**> | ADDED / EXCLUDED / ADDED_EXCLUDED / NONE — whether the term is already a keyword or a negative. | [optional]
**match_type** | Option<**String**> | How the term matched (BROAD, PHRASE, EXACT, NEAR_PHRASE, NEAR_EXACT). | [optional]
**campaign_id** | Option<**String**> |  | [optional]
**campaign_name** | Option<**String**> |  | [optional]
**ad_group_id** | Option<**String**> |  | [optional]
**ad_group_name** | Option<**String**> |  | [optional]
**impressions** | Option<**i32**> |  | [optional]
**clicks** | Option<**i32**> |  | [optional]
**cost_micros** | Option<**i32**> | Cost in micros of the account currency (divide by 1,000,000). | [optional]
**conversions** | Option<**f64**> |  | [optional]
**conversions_value** | Option<**f64**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


