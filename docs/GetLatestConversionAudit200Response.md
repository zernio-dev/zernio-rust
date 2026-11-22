# GetLatestConversionAudit200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**report** | [**models::ConversionAuditReport**](ConversionAuditReport.md) |  | 
**networks** | [**Vec<models::ConversionAuditAnswerNetworksInner>**](ConversionAuditAnswerNetworksInner.md) | Each ad network with its final setup and leak, computed exactly as the public report page shows them, best setup first. | 
**top_fixes** | [**Vec<models::ConversionAuditAnswerTopFixesInner>**](ConversionAuditAnswerTopFixesInner.md) | The few fixes that matter most, in the order the public report page lists them. | 
**fix_prompt** | **String** | A prompt to paste into a coding agent. It lists the report's findings, then connecting Zernio, sending conversions server-side and verifying them. | 
**public_report** | Option<[**models::ConversionAuditAnswerPublicReport**](ConversionAuditAnswerPublicReport.md)> |  | 
**host** | **String** | The normalized host the report is stored under. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


