# CreateStandaloneAdRequestCreativesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> | Exact name for this ad. Falls back to `<name> #N` (N = 1-based position). | [optional]
**headline** | **String** |  | 
**body** | **String** |  | 
**description** | Option<**String**> | Link description for this ad (link_data.description; video creatives: video_data.link_description). Falls back to the top-level `description`; when both are omitted Meta scrapes the destination URL's OG description. | [optional]
**image_url** | Option<**String**> | Image creative. Mutually exclusive with `video`. | [optional]
**video** | Option<[**models::CreateStandaloneAdRequestCreativesInnerVideo**](CreateStandaloneAdRequestCreativesInnerVideo.md)> |  | [optional]
**link_url** | **String** |  | 
**call_to_action** | **CallToAction** |  (enum: LEARN_MORE, SHOP_NOW, SIGN_UP, BOOK_TRAVEL, CONTACT_US, DOWNLOAD, GET_OFFER, GET_QUOTE, SUBSCRIBE, WATCH_MORE) | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


