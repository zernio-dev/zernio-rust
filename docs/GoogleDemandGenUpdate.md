# GoogleDemandGenUpdate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**final_url** | Option<**String**> |  | [optional]
**business_name** | Option<**String**> |  | [optional]
**headlines** | Option<**Vec<String>**> |  | [optional]
**long_headlines** | Option<**Vec<String>**> | Video ads only. | [optional]
**descriptions** | Option<**Vec<String>**> |  | [optional]
**call_to_action** | Option<**String**> | Image and carousel ads only. | [optional]
**images** | Option<[**models::GoogleDemandGenUpdateImages**](GoogleDemandGenUpdateImages.md)> |  | [optional]
**youtube_video_ids** | Option<**Vec<String>**> | Video ads only. | [optional]
**channels** | Option<**Vec<Channels>**> | Replaces the ad group's channel controls; only the listed channels serve. (enum: youtube_in_stream, youtube_in_feed, youtube_shorts, discover, gmail, display) | [optional]
**audience** | Option<[**models::GoogleDemandGenAudience**](GoogleDemandGenAudience.md)> |  | [optional]
**audience_id** | Option<**String**> | Attach an existing Google Audience by numeric id instead of audience. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


