# BusinessAgentSettings

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**agent_id** | **String** |  | 
**channel** | **String** |  | 
**rollout** | [**models::BusinessAgentSettingsRollout**](BusinessAgentSettingsRollout.md) |  | 
**handoff** | Option<[**models::BusinessAgentSettingsHandoff**](BusinessAgentSettingsHandoff.md)> |  | [optional]
**followup** | Option<[**models::BusinessAgentSettingsFollowup**](BusinessAgentSettingsFollowup.md)> |  | [optional]
**ai_audience** | Option<**AiAudience**> | EVERYONE answers all consumers; ALLOWLISTED_ONLY answers only the allowlist and needs no payment method. (enum: EVERYONE, ALLOWLISTED_ONLY, ) | [optional]
**never_say_phrases** | Option<**Vec<String>**> | Exact phrases the agent must never say. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


