# CtwaAdRequestBodyPlacements

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**publisher_platforms** | Option<**Vec<PublisherPlatforms>**> | Top-level platforms to deliver on. A position field below is only honoured when its parent platform is included here. (enum: facebook, instagram, threads, messenger, audience_network, whatsapp) | [optional]
**facebook_positions** | Option<**Vec<FacebookPositions>**> |  (enum: feed, right_hand_column, marketplace, video_feeds, story, search, instream_video, facebook_reels, facebook_reels_overlay, profile_feed, notification) | [optional]
**instagram_positions** | Option<**Vec<InstagramPositions>**> |  (enum: stream, story, explore, explore_home, reels, profile_feed, ig_search, profile_reels) | [optional]
**messenger_positions** | Option<**Vec<MessengerPositions>**> |  (enum: messenger_home, sponsored_messages, story) | [optional]
**audience_network_positions** | Option<**Vec<AudienceNetworkPositions>**> |  (enum: classic, rewarded_video) | [optional]
**threads_positions** | Option<**Vec<ThreadsPositions>**> |  (enum: threads_stream) | [optional]
**whatsapp_positions** | Option<**Vec<WhatsappPositions>**> |  (enum: status) | [optional]
**device_platforms** | Option<**Vec<DevicePlatforms>**> | Restrict by device. Omit to deliver on both mobile and desktop. (enum: mobile, desktop) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


