# BusinessAgentUiSkillInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | Option<**String**> |  | [optional]
**component_type** | **ComponentType** |  (enum: carousel_quick_reply, carousel_url, cta_url, flow, image, interactive_list, interactive_reply_buttons, location, location_request) | 
**status** | **Status** |  (enum: enabled, disabled) | 
**instruction** | **String** | When to send the component and everything needed to fill its fields. | 
**flow_id** | Option<**i32**> | Required for component_type flow, rejected otherwise. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


