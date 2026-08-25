# WebhookPayloadWhatsAppAccountNameStatusUpdatedName

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **Status** | Normalized from Meta's `decision` (REJECTED -> DECLINED, DEFERRED -> PENDING_REVIEW; the review is still open on DEFERRED, not a rejection). (enum: APPROVED, DECLINED, PENDING_REVIEW) | 
**requested_name** | Option<**String**> | The display name Meta reviewed. Null if Meta did not send one. | 
**rejection_reason** | Option<**String**> | Meta's free-form decline reason. Null on approval, or when Meta sends the literal string \"NONE\". | 
**display_phone_number** | Option<**String**> | The phone number this review is for, as Meta reported it. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


