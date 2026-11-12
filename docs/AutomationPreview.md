# AutomationPreview

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**evaluated_at** | **String** |  | 
**today** | [**String**](String.md) | Today in the ad account timezone. | 
**timezone** | **String** |  | 
**timezone_assumed** | **bool** | True when the ad account timezone is unknown and UTC was used. | 
**currency** | Option<**String**> |  | 
**hourly_through** | Option<**String**> | Where the hourly windows (`last_complete_hour`, `last_3h`, `today_so_far`) ended: the end of the latest hour a sync has settled. Null when the rule has none or they could not be read. | [optional]
**evaluated** | **i32** |  | 
**matched** | **i32** |  | 
**truncated** | **bool** | True when more subjects were judged than `limit` lists. | 
**subjects** | [**Vec<models::AutomationPreviewSubjectsInner>**](AutomationPreviewSubjectsInner.md) | Matches first, up to `limit`. | 
**groups** | Option<[**Vec<models::AutomationPreviewGroupsInner>**](AutomationPreviewGroupsInner.md)> | Each group's totals against the conditions, when the rule has `subjects.groups`. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


