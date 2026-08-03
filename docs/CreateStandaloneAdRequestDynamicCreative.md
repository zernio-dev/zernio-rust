# CreateStandaloneAdRequestDynamicCreative

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**image_urls** | Option<**Vec<String>**> | Pool of image URLs (1-10). Uploaded to the ad account and referenced by hash in the asset feed. Mutually exclusive with `videoUrls`. | [optional]
**video_urls** | Option<**Vec<String>**> | Pool of video URLs (1-10). Uploaded to the ad account and referenced by video id in the asset feed. No thumbnails are needed: Meta auto-generates a poster per video. Mutually exclusive with `imageUrls`; `adFormat` defaults to SINGLE_VIDEO. | [optional]
**bodies** | Option<**Vec<String>**> | Primary-text variations (the body copy). | [optional]
**titles** | Option<**Vec<String>**> | Headline variations. | [optional]
**descriptions** | Option<**Vec<String>**> | Description (link caption) variations. | [optional]
**link_urls** | Option<**Vec<String>**> | Destination URL variations. At least one is required unless `goal` is `lead_generation`. | [optional]
**call_to_action_types** | Option<**Vec<CallToActionTypes>**> | CTA-button variations. Required. (enum: LEARN_MORE, SHOP_NOW, SIGN_UP, BOOK_TRAVEL, CONTACT_US, DOWNLOAD, GET_OFFER, GET_QUOTE, SUBSCRIBE, WATCH_MORE, ADD_TO_CART, APPLY_NOW, BOOK_NOW, BUY_TICKETS, DONATE, DONATE_NOW, GET_DIRECTIONS, GET_SHOWTIMES, LISTEN_NOW, ORDER_NOW, PLAY_GAME, REQUEST_TIME, SEE_MENU, START_ORDER, INSTALL_MOBILE_APP, USE_APP, REGISTER, JOIN, ATTEND, REQUEST_DEMO, VIEW_QUOTE, APPLY, SEE_MORE, BUY_NOW) | [optional]
**ad_format** | Option<**AdFormat**> | Asset-feed ad format. Must match the pool: SINGLE_IMAGE / CAROUSEL_IMAGE require `imageUrls`, SINGLE_VIDEO requires `videoUrls` (400 otherwise). Defaults to SINGLE_IMAGE with `imageUrls`, SINGLE_VIDEO with `videoUrls`. (enum: SINGLE_IMAGE, CAROUSEL_IMAGE, SINGLE_VIDEO) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


