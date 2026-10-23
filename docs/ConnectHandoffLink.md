# ConnectHandoffLink

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**uuid::Uuid**> | Pass to `GET /v1/connect/handoffs/{handoffId}`. | [optional]
**url** | Option<**String**> | Short link to encode in the QR code. It opens the welcome screen on the phone. | [optional]
**expires_at** | Option<**String**> | When `url` stops working (30 minutes). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


