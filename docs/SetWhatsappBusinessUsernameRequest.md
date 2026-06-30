# SetWhatsappBusinessUsernameRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account ID | 
**username** | **String** | Desired username. Letters, digits, period, and underscore only. Must contain at least one letter. No leading, trailing, or consecutive periods. No www prefix. No domain TLD suffix.  | 
**transfer_action** | Option<**TransferAction**> | Pass `force_transfer` to request a transfer if the username is held by another account (enum: none, force_transfer) | [optional][default to None]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


