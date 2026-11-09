# GetEvent200ResponseDeliveriesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | Option<**String**> |  | [optional]
**destination_id** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: metaads, googleads, linkedinads, tiktokads, openaiads, pinterestads, redditads, ) | [optional]
**status** | Option<**Status**> |  (enum: sent, retrying, failed) | [optional]
**attempt** | Option<**i32**> | Send attempt (1 = the first). | [optional]
**error** | Option<**String**> |  | [optional]
**error_code** | Option<**String**> |  | [optional]
**sent_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


