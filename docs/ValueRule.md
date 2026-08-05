# ValueRule

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Platform rule id. Echo it on `PUT` to KEEP this rule, omit it to CREATE a new one. A rule left out of the array entirely is DELETED.  | [optional]
**name** | **String** |  | 
**adjust_sign** | **AdjustSign** | Direction of the adjustment. There is no signed value field. (enum: INCREASE, DECREASE) | 
**adjust_value** | **i32** | Unsigned percentage magnitude. `INCREASE` accepts 1-1000, `DECREASE` accepts 1-90. 0 is out of range on both.  | 
**status** | Option<**String**> | Meta returns `ACTIVE` here but documents no enum for the field. Treat it as a passthrough: echo whatever the `GET` returned, and do not synthesize values.  | [optional]
**criteria** | [**Vec<models::ValueRuleCriterion>**](ValueRuleCriterion.md) | All criteria on a rule must match for the rule to fire. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


