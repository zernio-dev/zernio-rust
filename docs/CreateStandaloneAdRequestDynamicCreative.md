# CreateStandaloneAdRequestDynamicCreative

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**image_urls** | **Vec<String>** | Pool of image URLs (1-10). Uploaded to the ad account and referenced by hash in the asset feed. | 
**bodies** | Option<**Vec<String>**> | Primary-text variations (the body copy). | [optional]
**titles** | Option<**Vec<String>**> | Headline variations. | [optional]
**descriptions** | Option<**Vec<String>**> | Description (link caption) variations. | [optional]
**link_urls** | Option<**Vec<String>**> | Destination URL variations. At least one is required unless `goal` is `lead_generation`. | [optional]
**call_to_action_types** | Option<**Vec<CallToActionTypes>**> | CTA-button variations. Required. (enum: LEARN_MORE, SHOP_NOW, SIGN_UP, BOOK_TRAVEL, CONTACT_US, DOWNLOAD, GET_OFFER, GET_QUOTE, SUBSCRIBE, WATCH_MORE, REGISTER, JOIN, ATTEND, REQUEST_DEMO, VIEW_QUOTE, APPLY, SEE_MORE, BUY_NOW) | [optional]
**ad_format** | Option<**AdFormat**> | Asset-feed ad format. Defaults to SINGLE_IMAGE. (enum: SINGLE_IMAGE, CAROUSEL_IMAGE) | [optional][default to SingleImage]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


