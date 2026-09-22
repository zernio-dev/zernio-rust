# CtwaAdRequestBodyCreativesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform_post_id** | Option<**String**> | Messaging and CTWA only. Platform post or reel ID, the same input boostPost takes as platformPostId. Facebook IDs become object_story_id; Instagram IDs become source_instagram_media_id using the connected Instagram identity. Mutually exclusive with objectStoryId and fresh creative fields. | [optional]
**existing_post_id** | Option<**String**> | Alias of platformPostId, kept for existing callers. Sending both with different values is a 400. | [optional]
**object_story_id** | Option<**String**> | Messaging and CTWA only. Raw Facebook pageId_postId reference, used as object_story_id even with an Instagram account. Mutually exclusive with platformPostId and fresh creative fields. | [optional]
**creative_features** | Option<**std::collections::HashMap<String, Inner>**> | Replaces the top-level creativeFeatures map for this item. Omit to inherit; an empty object clears inherited enrollment choices. (enum: OPT_IN, OPT_OUT) | [optional]
**headline** | Option<**String**> |  | [optional]
**body** | Option<**String**> | Primary text shown above the image / video. | [optional]
**image_url** | Option<**String**> | Image asset. Mutually exclusive with this entry's `video`. Required if neither `video` nor an existing post reference is supplied.  | [optional]
**video** | Option<[**models::CtwaAdRequestBodyCreativesInnerVideo**](CtwaAdRequestBodyCreativesInnerVideo.md)> |  | [optional]
**welcome_message** | Option<[**models::CtwaAdRequestBodyCreativesInnerWelcomeMessage**](CtwaAdRequestBodyCreativesInnerWelcomeMessage.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


