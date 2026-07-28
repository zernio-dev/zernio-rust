# PreflightSmsRegistration200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**composed** | Option<[**models::PreflightSmsRegistration200ResponseComposed**](PreflightSmsRegistration200ResponseComposed.md)> |  | [optional]
**advisories** | Option<[**Vec<models::PreflightSmsRegistration200ResponseAdvisoriesInner>**](PreflightSmsRegistration200ResponseAdvisoriesInner.md)> |  | [optional]
**verdict** | Option<**Verdict**> |  (enum: pass, warn, fail, unreviewed) | [optional]
**ai_unavailable** | Option<**bool**> | True when the AI portion of the check could not run; advisories then contain only deterministic findings. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


