# GetAccountHealth200ResponseSendCap

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**limit** | Option<**i32**> | Today's cap: the base cap, doubled after 14 days of sending with no spam signal. | [optional]
**base_limit** | Option<**i32**> | The cap before doubling. | [optional]
**doubled** | Option<**bool**> |  | [optional]
**doubles_at** | Option<**String**> | When the cap doubles if the mailbox sends every day from now on and raises no spam signal. Null once doubled, with a manual limit, and on IMAP. | [optional]
**used** | Option<**i32**> |  | [optional]
**resets_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


