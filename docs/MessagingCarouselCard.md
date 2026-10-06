# MessagingCarouselCard

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**image_url** | **String** | Card image. Uploaded to the ad account and sent as the card image_hash (by URL on validateOnly). | 
**headline** | Option<**String**> | Card title (Meta name). | [optional]
**description** | Option<**String**> | Card description, under the title. | [optional]
**call_to_action** | Option<**String**> | Optional. Must equal the destination's messaging call to action (WHATSAPP_MESSAGE for whatsapp, MESSAGE_PAGE for messenger, INSTAGRAM_MESSAGE for instagram_direct; with `destinations` the first one listed). Any other value is a 400 naming the card, because Meta refuses a carousel whose cards do not all open the destination. | [optional]
**link_url** | Option<**String**> | Not accepted: a 400. The card tap opens the conversation, not a website. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


