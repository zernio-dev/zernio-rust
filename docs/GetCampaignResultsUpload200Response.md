# GetCampaignResultsUpload200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**upload_id** | **String** |  | 
**status** | **Status** |  (enum: queued, done, failed) | 
**source** | **Source** |  (enum: api, csv, hubspot) | 
**rows_received** | **i32** |  | 
**rows_matched** | **i32** |  | 
**rows_unmatched** | **i32** |  | 
**unmatched** | [**Vec<models::GetCampaignResultsUpload200ResponseUnmatchedInner>**](GetCampaignResultsUpload200ResponseUnmatchedInner.md) |  | 
**created_at** | **String** |  | 
**completed_at** | Option<**String**> |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


