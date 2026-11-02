# GetAdAccountHealth200ResponseChecksInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **Id** |  (enum: account_status, payment, spend_cap, page, instagram, lead_terms, pixel, whatsapp, last_refusal) | 
**status** | **Status** |  (enum: ok, warning, error, missing, unknown) | 
**title** | **String** |  | 
**message** | **String** |  | 
**code** | Option<**String**> | When the check is not `ok`: the error code a create refused for this reason returns. | [optional]
**hint** | Option<**String**> |  | [optional]
**fix** | Option<[**models::GetAdAccountHealth200ResponseBlockersInnerFix**](GetAdAccountHealth200ResponseBlockersInnerFix.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


