# SetConversationThreadControlRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Social account ID | 
**action** | **Action** |  (enum: release, take, pass) | 
**target** | Option<**Target**> | With action pass: send control to Meta Business Agent instead of the escalation partner. (enum: ai_agent) | [optional]
**metadata** | Option<**String**> | Free-form note forwarded verbatim to the app receiving control (its messaging_handovers webhook). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


