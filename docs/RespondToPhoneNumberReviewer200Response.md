# RespondToPhoneNumberReviewer200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | Option<**Status**> | `resubmitted` when corrections were submitted, `replied` when it was message-only. (enum: resubmitted, replied) | [optional]
**posted** | Option<**bool**> | Whether a message/attachments were posted to the reviewer. | [optional]
**phone_number** | Option<[**models::RemediatePhoneNumber200ResponsePhoneNumber**](RemediatePhoneNumber200ResponsePhoneNumber.md)> |  | [optional]
**siblings_resubmitted** | Option<**i32**> | Other numbers on the same registration the correction fanned out to. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


