# GohighlevelAudienceSync

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**tag** | **String** | The HighLevel tag, lowercased. | 
**status** | **Status** |  (enum: syncing, ready, error) | 
**member_count** | **i32** | Contacts with the tag uploaded to the audiences so far. | 
**last_error** | Option<**String**> |  | 
**audiences** | [**Vec<models::GohighlevelAudienceSyncAudiencesInner>**](GohighlevelAudienceSyncAudiencesInner.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


