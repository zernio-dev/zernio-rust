# CreateGoogleBusinessLocation200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | Option<**bool**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**validate_only** | Option<**bool**> | Present and true when validateOnly was requested. | [optional]
**location** | Option<**std::collections::HashMap<String, serde_json::Value>**> | The location as Google returns it. `id` is present on a real create. | [optional]
**voice_of_merchant_state** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Verification state of the new listing; null if Google could not return it. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


