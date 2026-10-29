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
**call_to_action_types** | Option<**Vec<CallToActionTypes>**> | CTA-button variations. Required. (enum: BOOK_TRAVEL, CONTACT_US, DONATE, DONATE_NOW, DOWNLOAD, GET_DIRECTIONS, GO_LIVE, INTERESTED, LEARN_MORE, SEE_DETAILS, LIKE_PAGE, MESSAGE_PAGE, RAISE_MONEY, SAVE, SEND_TIP, SHOP_NOW, SIGN_UP, VIEW_INSTAGRAM_PROFILE, INSTAGRAM_MESSAGE, LOYALTY_LEARN_MORE, PURCHASE_GIFT_CARDS, PAY_TO_ACCESS, SEE_MORE, TRY_IN_CAMERA, WHATSAPP_LINK, GET_IN_TOUCH, TRY_NOW, ASK_A_QUESTION, START_A_CHAT, CHAT_NOW, ASK_US, CHAT_WITH_US, SHOP_ON_RETAILER, BOOK_NOW, CHECK_AVAILABILITY, ORDER_NOW, WHATSAPP_MESSAGE, GET_MOBILE_APP, INSTALL_MOBILE_APP, USE_MOBILE_APP, INSTALL_APP, USE_APP, PLAY_GAME, TRY_DEMO, WATCH_VIDEO, WATCH_MORE, OPEN_LINK, NO_BUTTON, LISTEN_MUSIC, MOBILE_DOWNLOAD, GET_OFFER, GET_OFFER_VIEW, BUY_NOW, BUY_TICKETS, UPDATE_APP, BET_NOW, ADD_TO_CART, SELL_NOW, GET_SHOWTIMES, LISTEN_NOW, GET_EVENT_TICKETS, REMIND_ME, SEARCH_MORE, PRE_REGISTER, SWIPE_UP_PRODUCT, SWIPE_UP_SHOP, PLAY_GAME_ON_FACEBOOK, VISIT_WORLD, OPEN_INSTANT_APP, JOIN_GROUP, GET_PROMOTIONS, SEND_UPDATES, INQUIRE_NOW, VISIT_PROFILE, CHAT_ON_WHATSAPP, EXPLORE_MORE, CONFIRM, JOIN_CHANNEL, MAKE_AN_APPOINTMENT, ASK_ABOUT_SERVICES, BOOK_A_CONSULTATION, GET_A_QUOTE, BUY_VIA_MESSAGE, ASK_FOR_MORE_INFO, VIEW_PRODUCT, VIEW_CHANNEL, WATCH_LIVE_VIDEO, JOIN_LIVE_VIDEO, IMAGINE, WATCH_NOW, STREAM_NOW, BUY_ACTIVITY_TICKETS, CALL, MISSED_CALL, CALL_NOW, CALL_ME, APPLY_NOW, BUY, GET_QUOTE, SUBSCRIBE, RECORD_NOW, VOTE_NOW, GIVE_FREE_RIDES, REGISTER_NOW, OPEN_MESSENGER_EXT, EVENT_RSVP, CIVIC_ACTION, SEND_INVITES, REFER_FRIENDS, REQUEST_TIME, SEE_MENU, SEARCH, TRY_IT, TRY_ON, LINK_CARD, DIAL_CODE, FIND_YOUR_GROUPS, START_ORDER) | [optional]
**ad_format** | Option<**AdFormat**> | Asset-feed ad format. Must match the pool: SINGLE_IMAGE / CAROUSEL_IMAGE require `imageUrls`, SINGLE_VIDEO requires `videoUrls` (400 otherwise). Defaults to SINGLE_IMAGE with `imageUrls`, SINGLE_VIDEO with `videoUrls`. (enum: SINGLE_IMAGE, CAROUSEL_IMAGE, SINGLE_VIDEO) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


