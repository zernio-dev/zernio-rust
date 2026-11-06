# AutomationTemplateInstallRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**inputs** | Option<**std::collections::HashMap<String, serde_json::Value>**> | A value for each input, by its `key`. Required inputs without a default must be sent. | [optional][default to {}]
**targets** | Option<[**Vec<models::AutomationTemplateInstallRequestTargetsInner>**](AutomationTemplateInstallRequestTargetsInner.md)> | Install several times in one call, for example on many ad accounts. Each target is its own install, all or nothing, and its `inputs` win over the shared `inputs`. A failed target leaves the others in place. | [optional]
**status** | Option<**Status**> | The status of every automation created. (enum: active, paused) | [optional][default to Paused]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


