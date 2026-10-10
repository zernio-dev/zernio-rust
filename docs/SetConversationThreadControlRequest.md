# SetConversationThreadControlRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Social account ID | 
**action** | **Action** | `request` is Facebook and Instagram only. `take` and `request` are refused with `platform_not_supported` on Instagram accounts connected with Instagram Login. (enum: release, take, pass, request) | 
**target** | Option<**Target**> | WhatsApp only. With action pass: send control to Meta Business Agent instead of the escalation partner. (enum: ai_agent) | [optional]
**target_app_id** | Option<**String**> | Facebook and Instagram only, required with action pass: the Meta app id receiving the thread. | [optional]
**metadata** | Option<**String**> | Free-form note forwarded verbatim to the app receiving control (its messaging_handovers webhook). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


