# CreateImessageOptInLinkRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**body** | **String** | Prefilled message text. Must contain the literal `[opt-in-code]` placeholder, e.g. \"Hi! My code is [opt-in-code]\". | 
**parameters** | Option<**std::collections::HashMap<String, String>**> | Custom key/values (e.g. leadId, campaign) echoed back on the opt-in message. | [optional]
**opt_in_code** | Option<**String**> | Your own code in place of the generated one (3-8 characters, no spaces or `#`, `!`, `-`). An unredeemed link lives 24 hours; re-issuing with the same code replaces it, and the earlier URL stops matching. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


