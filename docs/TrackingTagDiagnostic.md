# TrackingTagDiagnostic

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **String** | Platform check id (Meta: e.g. `pixel_missing_param_in_events`). | 
**title** | **String** |  | 
**description** | Option<**String**> |  | [optional]
**result** | **String** | The platform verdict (Meta: `passed`, `failed`, `warning`). | 
**action_url** | Option<**String**> | Where to fix it in the platform UI (Meta: Events Manager). | [optional]
**always_use_default_value** | Option<**bool**> | Record `defaultValue` even when the conversion sends its own value. | [optional]
**primary** | Option<**bool**> | Primary (counts toward bidding) or secondary (observation only). | [optional]
**counting_type** | Option<**CountingType**> | `one` = one conversion per ad interaction, `every` = each conversion. (enum: one, every) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


