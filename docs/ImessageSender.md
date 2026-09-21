# ImessageSender

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Account id (use it with the inbox endpoints' accountId) | [optional]
**platform** | Option<**Platform**> |  (enum: imessage) | [optional]
**sender** | Option<**String**> | The sender handle (E.164 phone or email) | [optional]
**opt_in_link** | Option<**String**> | imessage:// deep link that opens Messages on this sender with a prefilled text. Share it so contacts message you first (Apple only lets a sender reach contacts who wrote to it first). | [optional]
**display_name** | Option<**String**> |  | [optional]
**profile_id** | Option<**String**> |  | [optional]
**provider** | Option<**String**> | Delivery provider backing this sender (e.g. loopmessage) | [optional]
**sender_verified** | Option<**bool**> | Whether the provider confirmed the sender as active at registration time | [optional]
**is_active** | Option<**bool**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


