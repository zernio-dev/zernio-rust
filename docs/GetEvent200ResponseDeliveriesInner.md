# GetEvent200ResponseDeliveriesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | Option<**String**> |  | [optional]
**destination_id** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: metaads, googleads, linkedinads, tiktokads, openaiads, pinterestads, redditads, ) | [optional]
**status** | Option<**Status**> | `dropped`: not sent because the visitor did not consent; `errorCode` says why (`consent_denied` or `consent_missing`). (enum: sent, retrying, failed, dropped) | [optional]
**attempt** | Option<**i32**> | Send attempt (1 = the first). | [optional]
**error** | Option<**String**> |  | [optional]
**error_code** | Option<**String**> |  | [optional]
**sent_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


