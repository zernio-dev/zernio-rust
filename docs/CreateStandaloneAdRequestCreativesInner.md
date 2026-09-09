# CreateStandaloneAdRequestCreativesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**promotion** | Option<[**models::MetaPromotion**](MetaPromotion.md)> | Overrides the top-level offer for this item. Omit to inherit; null disables the inherited offer. | [optional]
**creative_features** | Option<**std::collections::HashMap<String, Inner>**> | Replaces the entire top-level creativeFeatures map for this item. Omit to inherit; an empty map clears these defaults. (enum: OPT_IN, OPT_OUT) | [optional]
**name** | Option<**String**> | Exact name for this ad. Falls back to `<name> #N` (N = 1-based position). | [optional]
**headline** | **String** |  | 
**body** | **String** |  | 
**description** | Option<**String**> | Link description for this ad (link_data.description; video creatives: video_data.link_description). Falls back to the top-level `description`; when both are omitted Meta scrapes the destination URL's OG description. | [optional]
**image_url** | Option<**String**> | Image creative. Mutually exclusive with `video`. | [optional]
**video** | Option<[**models::CreateStandaloneAdRequestCreativesInnerVideo**](CreateStandaloneAdRequestCreativesInnerVideo.md)> |  | [optional]
**link_url** | **String** |  | 
**call_to_action** | **CallToAction** |  (enum: LEARN_MORE, SHOP_NOW, SIGN_UP, BOOK_TRAVEL, CONTACT_US, DOWNLOAD, GET_OFFER, GET_QUOTE, SUBSCRIBE, WATCH_MORE, ADD_TO_CART, APPLY_NOW, BOOK_NOW, BUY_TICKETS, DONATE, DONATE_NOW, GET_DIRECTIONS, GET_SHOWTIMES, LISTEN_NOW, ORDER_NOW, PLAY_GAME, REQUEST_TIME, SEE_MENU, START_ORDER, INSTALL_MOBILE_APP, USE_APP) | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


