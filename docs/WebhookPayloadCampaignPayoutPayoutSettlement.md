# WebhookPayloadCampaignPayoutPayoutSettlement

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**entry_id** | **String** | The ledger settlement entry. | 
**amount_cents** | **i32** |  | 
**external_reference** | Option<**String**> |  | 
**recorded** | **bool** | True when the payout was made outside Zernio and only recorded here; false when Zernio moved the money through the treasury. | 
**transfer_id** | Option<**String**> | Treasury settlement only: the Zernio transfer that moved the money. The creator receives amountCents in full. | [optional]
**fee_cents** | Option<**i32**> | Treasury settlement only: the transfer fee, added on top of amountCents. | [optional]
**total_cents** | Option<**i32**> | Treasury settlement only: debited from your balance, amountCents plus feeCents. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


