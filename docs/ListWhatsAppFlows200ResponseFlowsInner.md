# ListWhatsAppFlows200ResponseFlowsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**status** | Option<**Status**> |  (enum: DRAFT, PUBLISHED, DEPRECATED, BLOCKED, THROTTLED) | [optional]
**categories** | Option<**Vec<String>**> |  | [optional]
**validation_errors** | Option<**Vec<serde_json::Value>**> |  | [optional]
**version** | Option<**i32**> | 1-based version within the flow's clone lineage (Zernio-tracked; Meta has no native versioning). Standalone flows are version 1. | [optional]
**lineage_id** | Option<**String**> | Stable group key for the flow's version lineage (the root flow's ID). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


