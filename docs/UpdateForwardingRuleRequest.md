# UpdateForwardingRuleRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**api_secret** | Option<**String**> |  | [optional]
**event_name_map** | Option<**std::collections::HashMap<String, String>**> | Your event name to the name this destination gets, such as `{ \"Lead\": \"Purchase\" }`. Names not in the map are sent unchanged.  A target spelled like a standard event in another case or form (`purchase`, `generate_lead`) is saved as the standard name (`Purchase`, `Lead`), so each platform gets its own standard event.  `eventNames` and `valueCondition` are checked against the name and value as received, before renaming. The event id is never changed, so deduplication still works. | [optional]
**value_override** | Option<[**models::ForwardingRuleValueOverride**](ForwardingRuleValueOverride.md)> |  | [optional]
**value_condition** | Option<[**models::ForwardingRuleValueCondition**](ForwardingRuleValueCondition.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


