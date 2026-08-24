# CreateSipTrunk201Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**label** | Option<**String**> |  | [optional]
**sip_host** | Option<**String**> |  | [optional]
**sip_port** | Option<**i32**> |  | [optional]
**transport** | Option<**Transport**> |  (enum: tls, tcp, udp) | [optional]
**termination** | Option<[**models::CreateSipTrunk201ResponseTermination**](CreateSipTrunk201ResponseTermination.md)> |  | [optional]
**numbers_attached** | Option<**i32**> |  | [optional]
**created_at** | Option<**String**> |  | [optional]
**digest_password** | Option<**String**> | SIP digest password, shown only in this response. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


