# AdjustConversionsRequestAdjustmentsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**adjustment_type** | **AdjustmentType** |  (enum: RETRACTION, RESTATEMENT, ENHANCEMENT) | 
**adjustment_time** | **f64** | When the adjustment occurred, unix seconds. | 
**order_id** | Option<**String**> | Transaction ID of the original conversion (the `eventId` you sent). Recommended; required for ENHANCEMENT. | [optional]
**gclid** | Option<**String**> | Alternative key — the original click ID. Pair with `conversionTime`. Not valid for ENHANCEMENT. | [optional]
**conversion_time** | Option<**f64**> | The original conversion's time, unix seconds. Required when identifying by `gclid`. | [optional]
**restatement_value** | Option<**f64**> | RESTATEMENT only — the corrected TOTAL conversion value. | [optional]
**currency** | Option<**String**> | RESTATEMENT only — ISO 4217 currency for `restatementValue`. | [optional]
**user** | Option<[**models::AdjustConversionsRequestAdjustmentsInnerUser**](AdjustConversionsRequestAdjustmentsInnerUser.md)> |  | [optional]
**user_agent** | Option<**String**> | ENHANCEMENT only — the original conversion's user agent (improves match quality). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


