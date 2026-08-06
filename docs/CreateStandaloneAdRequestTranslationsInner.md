# CreateStandaloneAdRequestTranslationsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**locale** | **String** | Language code, resolved to Meta's numeric locale id. Bare codes target the '(All)' umbrella (`es` = every Spanish variant); region-qualified codes target the variant (`pt_BR`, `en_GB`). | 
**headline** | **String** | Headline for this language. REQUIRED, and must differ from every other locale and from the ad's top-level headline. | 
**body** | **String** | Primary text for this language. REQUIRED, and must differ from every other locale and from the ad's top-level body. | 
**description** | **String** | Link description for this language. REQUIRED, and must differ from every other locale and from the ad's top-level description. | 
**link_url** | Option<**String**> | Destination URL for this language. Inherits the ad's top-level `linkUrl` when omitted, and requires it to be present (400 otherwise): the top-level URL is the destination for every locale you did not override. Unlike text, identical URLs across locales are fine (they share one asset). | [optional]
**image_url** | Option<**String**> | Image for this language. Inherits the ad's `imageUrl` when omitted. The feed is all-image OR all-video. | [optional]
**video_url** | Option<**String**> | Video for this language. Inherits the ad's `video.url` when omitted. The feed is all-image OR all-video. | [optional]
**thumbnail_url** | Option<**String**> | Poster frame for this language's video. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


