# GoogleDemandGenInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_group_name** | Option<**String**> | Defaults to the ad name. | [optional]
**final_url** | **String** |  | 
**business_name** | **String** |  | 
**headlines** | **Vec<String>** | Distinct texts. A carousel ad takes exactly one. | 
**long_headlines** | Option<**Vec<String>**> | Video ads only, and required there. | [optional]
**descriptions** | **Vec<String>** | A carousel ad takes exactly one. | 
**call_to_action** | Option<**String**> | Image and carousel ads only. Call to action text such as 'Learn more'; Google picks one when omitted. | [optional]
**images** | [**models::GoogleDemandGenInputImages**](GoogleDemandGenInputImages.md) |  | 
**youtube_video_ids** | Option<**Vec<String>**> | Makes the ad a video responsive ad. | [optional]
**carousel_cards** | Option<[**Vec<models::GoogleDemandGenInputCarouselCardsInner>**](GoogleDemandGenInputCarouselCardsInner.md)> | Makes the ad a carousel ad. Each card needs its own image (no two cards may share one); use the same image shape on every card. Card images are uploaded to the account's asset library before the campaign is created, validateOnly included (Google checks cards against existing images; identical images are reused, not duplicated). | [optional]
**channels** | Option<**Vec<Channels>**> | Channel controls on the ad group. Only the listed channels serve; omit to serve on all of them. (enum: youtube_in_stream, youtube_in_feed, youtube_shorts, discover, gmail, display) | [optional]
**audience** | Option<[**models::GoogleDemandGenAudience**](GoogleDemandGenAudience.md)> |  | [optional]
**audience_id** | Option<**String**> | Attach an existing Google Audience by numeric id instead of audience. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


