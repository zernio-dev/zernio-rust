# AutomationPostSubjects

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**each** | **Each** |  (enum: post) | 
**profile_id** | **String** | The profile whose posts are checked. | 
**account_ids** | Option<**Vec<String>**> | Only posts of these accounts. Each must be active on the profile. | [optional]
**published_within** | Option<**String**> | How far back posts are checked, by when they were published. Whole days, from `1d` to `30d` (`48h` is 2 days). | [optional][default to 7d]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


