# CtwaAdRequestBodyWelcomeMessage

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **String** | Greeting shown when the chat opens. Replaces Meta's default (\"Hi! Can we help you?\"). | 
**prefill_text** | Option<**String**> | Message put into the user's text input, ready to send. Replaces Meta's default (\"Hi! I want more info.\"). Lets one ad steer the opening message toward what it promotes (e.g. a specific product). Exactly one of prefillText or quickReplies. | [optional]
**quick_replies** | Option<[**Vec<models::CtwaAdRequestBodyWelcomeMessageQuickRepliesInner>**](CtwaAdRequestBodyWelcomeMessageQuickRepliesInner.md)> | Tappable chips under the greeting instead of a prefilled message. Exactly one of prefillText or quickReplies. Put your own campaign or ad key in each payload: the tap arrives on the messages webhook with that payload even where Meta delivers no ad referral (Pages owned by an EU business under the Europe/Japan Messenger restrictions).  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


