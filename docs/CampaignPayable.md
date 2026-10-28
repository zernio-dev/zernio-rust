# CampaignPayable

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**participant_id** | **String** |  | 
**creator** | [**models::WebhookPayloadCampaignSubmissionCreator**](WebhookPayloadCampaignSubmissionCreator.md) |  | 
**payable_cents** | **i32** | The participant's whole payable balance. | 
**entries** | **Vec<String>** | Ids of the newest ledger entries into payable that add up to the balance (up to 200). | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


