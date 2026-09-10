# CreateInboxConversationRequestTemplateCardsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**card_index** | **i32** | The card's card_index in the approved template. | 
**params** | Option<**Vec<String>**> | Values for this card's own body variables, in the card's own {{1}}, {{2}}, ... order (or named-slot order of appearance). | [optional]
**header_media** | Option<[**models::CreateInboxConversationRequestTemplateCardsInnerHeaderMedia**](CreateInboxConversationRequestTemplateCardsInnerHeaderMedia.md)> |  | [optional]
**buttons** | Option<[**Vec<models::CreateInboxConversationRequestTemplateCardsInnerButtonsInner>**](CreateInboxConversationRequestTemplateCardsInnerButtonsInner.md)> | Values for this card's own buttons, each addressed by the button's index within the card. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


