# OrderImessageSenderRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** |  | 
**kind** | **Kind** |  (enum: phone, email) | 
**region** | Option<**Region**> | Required for phone senders. Without availableNumberId the number is carrier-assigned in this region and revealed once the sender activates. (enum: US, GB) | [optional]
**available_number_id** | Option<**String**> | A number from GET /v1/imessage/senders/available-numbers. It is assigned and activated on order instead of waiting for provisioning. Phone senders only. | [optional]
**zip_code** | Option<**String**> | US phone senders only. Preferred area for a carrier-assigned number (ignored with availableNumberId). | [optional]
**email_name** | Option<**String**> | Local part for email senders (required for kind: email) | [optional]
**email_domain** | Option<**String**> | Domain for email senders (required for kind: email) | [optional]
**display_name** | Option<**String**> |  | [optional]
**purchase_intent_id** | Option<**String**> | Idempotency key for safe retries | [optional]
**contact** | Option<[**models::OrderImessageSenderRequestContact**](OrderImessageSenderRequestContact.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


