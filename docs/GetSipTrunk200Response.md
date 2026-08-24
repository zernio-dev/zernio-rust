# GetSipTrunk200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**label** | Option<**String**> |  | [optional]
**sip_host** | Option<**String**> |  | [optional]
**sip_port** | Option<**i32**> |  | [optional]
**transport** | Option<**Transport**> |  (enum: tls, tcp, udp) | [optional]
**termination** | Option<[**models::ListSipTrunks200ResponseTrunksInnerTermination**](ListSipTrunks200ResponseTrunksInnerTermination.md)> |  | [optional]
**numbers_attached** | Option<**i32**> |  | [optional]
**created_at** | Option<**String**> |  | [optional]
**numbers** | Option<[**Vec<models::GetSipTrunk200ResponseNumbersInner>**](GetSipTrunk200ResponseNumbersInner.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


