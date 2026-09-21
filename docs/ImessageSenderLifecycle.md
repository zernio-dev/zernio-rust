# ImessageSenderLifecycle

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**kind** | Option<**Kind**> |  (enum: phone, email) | [optional]
**region** | Option<**Region**> |  (enum: US, GB, ) | [optional]
**handle** | Option<**String**> | The sender handle once activation assigns it | [optional]
**opt_in_link** | Option<**String**> | imessage:// deep link that opens Messages on this sender with a prefilled text. Share it so contacts message you first (Apple only lets a sender reach contacts who wrote to it first); null until the handle is assigned. | [optional]
**status** | Option<**Status**> |  (enum: ordering, activating, active, suspended, canceled, failed) | [optional]
**price_cents** | Option<**i32**> | Monthly price billed while the sender is active | [optional]
**provider** | Option<**String**> |  | [optional]
**profile_id** | Option<**String**> |  | [optional]
**display_name** | Option<**String**> |  | [optional]
**failure_reason** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> | The messaging account created at activation | [optional]
**created_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


