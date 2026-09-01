# UpdateAdRequestCreative

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**headline** | Option<**String**> | Meta and LinkedIn (TikTok has no headline slot) | [optional]
**body** | Option<**String**> |  | [optional]
**description** | Option<**String**> | Link description slot (Meta `link_data.description` / `video_data.link_description`, LinkedIn creative description). | [optional]
**call_to_action** | Option<**String**> |  | [optional]
**link_url** | Option<**String**> |  | [optional]
**image_url** | Option<**String**> |  | [optional]
**video_url** | Option<**String**> |  | [optional]
**video_id** | Option<**String**> | Meta only. Reuse an already-uploaded ad video (from POST /v1/ads/videos or GET /v1/ads/videos) instead of re-uploading via videoUrl. | [optional]
**existing_creative_id** | Option<**String**> | Meta only. Repoint the ad at an existing library creative (from GET /v1/ads/creatives); all other creative fields are ignored. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


