# TrackingWindow

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**post_id** | **String** | The external post being tracked | 
**account_id** | **String** |  | 
**platform** | **String** |  | 
**platform_post_id** | **String** | The post's id on the platform | 
**starts_at** | **String** |  | 
**ends_at** | **String** |  | 
**status** | **Status** |  (enum: open, completing, completed, cancelled) | 
**final_read_at** | Option<**String**> | When the closing read ran. Null until then. | 
**completion_reason** | Option<**CompletionReason**> | How the window closed. Null while it is open. (enum: final_read, unreachable, post_deleted, cancelled, ) | 
**requested_by** | **String** |  | 
**latest** | [**models::TrackingWindowLatest**](TrackingWindowLatest.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


