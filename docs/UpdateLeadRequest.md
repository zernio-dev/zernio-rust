# UpdateLeadRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **Status** |  (enum: new, contacted, unreachable, qualified, converted, disqualified) | 
**value** | Option<**f64**> | Deal value; requires currency. | [optional]
**currency** | Option<**String**> | ISO 4217 code. | [optional]
**account_id** | Option<**String**> | Required when `{id}` is a Meta leadgenId: the facebook or metaads account that received the lead. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


