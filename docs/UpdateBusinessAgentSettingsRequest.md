# UpdateBusinessAgentSettingsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**rollout** | Option<[**models::UpdateBusinessAgentSettingsRequestRollout**](UpdateBusinessAgentSettingsRequestRollout.md)> |  | [optional]
**handoff** | Option<[**models::UpdateBusinessAgentSettingsRequestHandoff**](UpdateBusinessAgentSettingsRequestHandoff.md)> |  | [optional]
**followup** | Option<[**models::UpdateBusinessAgentSettingsRequestFollowup**](UpdateBusinessAgentSettingsRequestFollowup.md)> |  | [optional]
**ai_audience** | Option<**AiAudience**> |  (enum: EVERYONE, ALLOWLISTED_ONLY) | [optional]
**never_say_phrases** | Option<**Vec<String>**> | Exact phrases the agent must never say; the full replacement list. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


