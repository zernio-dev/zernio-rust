# WorkflowNode

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Stable node id referenced by edges | 
**r#type** | **Type** |  (enum: trigger, send_message, wait_for_reply, condition, set_variable, delay, webhook, handoff, end) | 
**config** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Type-specific settings. trigger: { keywords:[string], matchType: any|contains|exact|regex, onlyFirstMessage:boolean }. send_message: { messageType: text|template|media|interactive, text, template:{name,language,variableMapping}, media:{mediaType,url,caption}, interactive } (template/interactive are WhatsApp-only). wait_for_reply: { timeoutMinutes:int, saveAs:string }. condition: { rules:[{ id, variable, operator: equals|not_equals|contains|not_contains|starts_with|ends_with|exists|not_exists|matches, value }] }. set_variable: { assignments:[{ name, value }] }. delay: { delayMinutes:int }. webhook: { url, method, headers, bodyTemplate, saveAs }. handoff: { note, assignTo }. String fields support {{variable}} interpolation.  | [optional]
**position** | Option<[**models::WorkflowNodePosition**](WorkflowNodePosition.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


