# ConsentDrop

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**event_index** | Option<**i32**> | Index into the events sent to this destination. | [optional]
**event_id** | Option<**String**> |  | [optional]
**reason** | Option<**Reason**> | `consent_denied`: a signal the platform needs is `DENIED`. `consent_missing`: the visitor is in the EEA, UK or CH and the signal was never given. (enum: consent_denied, consent_missing) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


