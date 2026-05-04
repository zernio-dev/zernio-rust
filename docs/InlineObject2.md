# InlineObject2

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **String** | Human-readable error message suitable for end-user display. | 
**code** | **Code** | Machine-readable error code. Stable across versions. (enum: PAYMENT_REQUIRED) | 
**reason** | **Reason** | Discriminator for which gate fired. (enum: free_tier_exceeded, twitter_passthrough, enterprise_required) | 
**documentation_url** | Option<**String**> | Link to the relevant documentation page. | [optional]
**dashboard_url** | Option<**String**> | Deep-link to send the end-user to. For `free_tier_exceeded` and `twitter_passthrough` this is the Zernio billing tab. For `enterprise_required` this is the Zernio enterprise contact page.  | [optional]
**details** | Option<[**models::InlineObject2Details**](InlineObject2Details.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


