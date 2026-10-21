# SendWhatsAppConversion200ResponseFailuresInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**event_index** | Option<**i32**> | Index into the submitted events array. | [optional]
**event_id** | Option<**String**> | Echoes back the eventId of the failed event. | [optional]
**message** | Option<**String**> |  | [optional]
**code** | Option<[**models::SendConversions200ResponseFailuresInnerCode**](SendConversions200ResponseFailuresInnerCode.md)> |  | [optional]
**platform_error** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Meta's own error for the rejected event, with credentials redacted: `message`, `type`, `code`, `error_subcode`, `error_user_title`, `error_user_msg` and `fbtrace_id` when Meta sends them. `message` above already ends with `error_user_msg`. Absent when Meta returned no error body.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


