# CreateSipTrunkRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**label** | **String** | Display name for the trunk. | 
**sip_host** | **String** | Fully-qualified hostname inbound calls are delivered to (e.g. sip.rtc.elevenlabs.io, sip.retellai.com). | 
**sip_port** | Option<**i32**> | Defaults to 5061 for tls, 5060 otherwise. | [optional]
**transport** | Option<**Transport**> | Signaling transport toward sipHost. Default tls (with SRTP media). (enum: tls, tcp, udp) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


