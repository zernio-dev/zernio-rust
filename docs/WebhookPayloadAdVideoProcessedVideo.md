# WebhookPayloadAdVideoProcessedVideo

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Meta video id, as returned by the 202 upload response. | 
**platform_ad_account_id** | **String** | Meta ad account id (act_<n>) the video was uploaded to. | 
**status** | **Status** | `ready`: usable as `video.id` on the create endpoints. `error`: Meta could not process it; upload again. (enum: ready, error) | 
**error** | Option<**String**> | Meta's processing error when status is `error`, otherwise null. | 
**thumbnail_url** | Option<**String**> | Meta's auto-generated poster when status is `ready` and Meta produced one, otherwise null. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


