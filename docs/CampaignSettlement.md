# CampaignSettlement

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**entry_id** | **String** | The ledger settlement entry. | 
**participant_id** | **String** |  | 
**amount_cents** | **i32** |  | 
**external_reference** | Option<**String**> |  | 
**payable_cents** | **i32** | Payable balance left after this settlement. | 
**settled_at** | **String** |  | 
**transfer_id** | Option<**String**> | Treasury settlement only: the Zernio transfer that moved the money. The creator receives amountCents in full. | [optional]
**fee_cents** | Option<**i32**> | Treasury settlement only: the transfer fee, added on top of amountCents. | [optional]
**total_cents** | Option<**i32**> | Treasury settlement only: debited from your balance, amountCents plus feeCents. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


