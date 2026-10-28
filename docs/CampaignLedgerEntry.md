# CampaignLedgerEntry

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**kind** | **Kind** |  (enum: accrual, approval, hold_release, adjustment, settling, settlement, reversal, topup, transfer, fee) | 
**amount_cents** | **i32** | Always positive; direction is given by debit and credit. | 
**debit** | [**models::LedgerAccountSide**](LedgerAccountSide.md) |  | 
**credit** | [**models::LedgerAccountSide**](LedgerAccountSide.md) |  | 
**hold_until** | Option<**String**> |  | 
**released_by_entry_id** | Option<**String**> |  | 
**reverses_entry_id** | Option<**String**> |  | 
**reference_type** | Option<**String**> |  | 
**reference_id** | Option<**String**> |  | 
**cause** | **String** |  | 
**external_reference** | Option<**String**> | The payout reference recorded with a settlement (your transfer or invoice id). | 
**actor** | **String** |  | 
**created_at** | **String** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


