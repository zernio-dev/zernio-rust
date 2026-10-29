# CreateStandaloneAdRequestCreativesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**creative_features** | Option<**std::collections::HashMap<String, Inner>**> | Replaces the entire top-level creativeFeatures map for this item. Omit to inherit; an empty map clears these defaults. (enum: OPT_IN, OPT_OUT) | [optional]
**name** | Option<**String**> | Exact name for this ad. Falls back to `<name> #N` (N = 1-based position). | [optional]
**headline** | **String** |  | 
**body** | **String** |  | 
**description** | Option<**String**> | Link description for this ad (link_data.description; video creatives: video_data.link_description). Falls back to the top-level `description`; when both are omitted Meta scrapes the destination URL's OG description. | [optional]
**image_url** | Option<**String**> | Image creative. Mutually exclusive with `video`. | [optional]
**video** | Option<[**models::CreateStandaloneAdRequestCreativesInnerVideo**](CreateStandaloneAdRequestCreativesInnerVideo.md)> |  | [optional]
**link_url** | **String** |  | 
**call_to_action** | **CallToAction** |  (enum: BOOK_TRAVEL, CONTACT_US, DONATE, DONATE_NOW, DOWNLOAD, GET_DIRECTIONS, GO_LIVE, INTERESTED, LEARN_MORE, SEE_DETAILS, LIKE_PAGE, MESSAGE_PAGE, RAISE_MONEY, SAVE, SEND_TIP, SHOP_NOW, SIGN_UP, VIEW_INSTAGRAM_PROFILE, INSTAGRAM_MESSAGE, LOYALTY_LEARN_MORE, PURCHASE_GIFT_CARDS, PAY_TO_ACCESS, SEE_MORE, TRY_IN_CAMERA, WHATSAPP_LINK, GET_IN_TOUCH, TRY_NOW, ASK_A_QUESTION, START_A_CHAT, CHAT_NOW, ASK_US, CHAT_WITH_US, SHOP_ON_RETAILER, BOOK_NOW, CHECK_AVAILABILITY, ORDER_NOW, WHATSAPP_MESSAGE, GET_MOBILE_APP, INSTALL_MOBILE_APP, USE_MOBILE_APP, INSTALL_APP, USE_APP, PLAY_GAME, TRY_DEMO, WATCH_VIDEO, WATCH_MORE, OPEN_LINK, NO_BUTTON, LISTEN_MUSIC, MOBILE_DOWNLOAD, GET_OFFER, GET_OFFER_VIEW, BUY_NOW, BUY_TICKETS, UPDATE_APP, BET_NOW, ADD_TO_CART, SELL_NOW, GET_SHOWTIMES, LISTEN_NOW, GET_EVENT_TICKETS, REMIND_ME, SEARCH_MORE, PRE_REGISTER, SWIPE_UP_PRODUCT, SWIPE_UP_SHOP, PLAY_GAME_ON_FACEBOOK, VISIT_WORLD, OPEN_INSTANT_APP, JOIN_GROUP, GET_PROMOTIONS, SEND_UPDATES, INQUIRE_NOW, VISIT_PROFILE, CHAT_ON_WHATSAPP, EXPLORE_MORE, CONFIRM, JOIN_CHANNEL, MAKE_AN_APPOINTMENT, ASK_ABOUT_SERVICES, BOOK_A_CONSULTATION, GET_A_QUOTE, BUY_VIA_MESSAGE, ASK_FOR_MORE_INFO, VIEW_PRODUCT, VIEW_CHANNEL, WATCH_LIVE_VIDEO, JOIN_LIVE_VIDEO, IMAGINE, WATCH_NOW, STREAM_NOW, BUY_ACTIVITY_TICKETS, CALL, MISSED_CALL, CALL_NOW, CALL_ME, APPLY_NOW, BUY, GET_QUOTE, SUBSCRIBE, RECORD_NOW, VOTE_NOW, GIVE_FREE_RIDES, REGISTER_NOW, OPEN_MESSENGER_EXT, EVENT_RSVP, CIVIC_ACTION, SEND_INVITES, REFER_FRIENDS, REQUEST_TIME, SEE_MENU, SEARCH, TRY_IT, TRY_ON, LINK_CARD, DIAL_CODE, FIND_YOUR_GROUPS, START_ORDER) | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


