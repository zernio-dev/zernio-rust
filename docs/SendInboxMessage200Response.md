# SendInboxMessage200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | Option<**bool**> |  | [optional]
**warnings** | Option<[**Vec<models::SendInboxMessage200ResponseWarningsInner>**](SendInboxMessage200ResponseWarningsInner.md)> | Present when a successful send ignored replyTo on Instagram or Facebook Messenger. The message was sent without a quote; do not retry it to apply the reply. | [optional]
**data** | Option<[**models::SendInboxMessage200ResponseData**](SendInboxMessage200ResponseData.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


