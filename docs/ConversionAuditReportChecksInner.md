# ConversionAuditReportChecksInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Stable check id, such as `pixels`, `server-side`, `first-party`, `consent`, `consent-timing` or `match-quality`. New checks can appear. | 
**title** | **String** |  | 
**status** | **Status** | `unknown` = the scan cannot see it from outside; `not-applicable` checks are left out of the score. (enum: pass, partial, fail, unknown, not-applicable) | 
**tier** | Option<**Tier**> | A `bonus` check can only add points, never cost them. (enum: essential, recommended, bonus) | [optional]
**weight** | **f64** |  | 
**detail** | **String** |  | 
**points_to_gain** | Option<**f64**> | Points the score gains when this check alone is fixed. | [optional]
**verify** | Option<[**models::ConversionAuditReportChecksInnerVerify**](ConversionAuditReportChecksInnerVerify.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


