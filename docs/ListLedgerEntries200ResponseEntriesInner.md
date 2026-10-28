# ListLedgerEntries200ResponseEntriesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**kind** | Option<**Kind**> |  (enum: accrual, approval, hold_release, adjustment, settling, settlement, reversal, topup, transfer, fee) | [optional]
**amount_cents** | Option<**i32**> | Always positive; direction is given by debit and credit | [optional]
**debit** | Option<[**models::LedgerAccountSide**](LedgerAccountSide.md)> |  | [optional]
**credit** | Option<[**models::LedgerAccountSide**](LedgerAccountSide.md)> |  | [optional]
**hold_until** | Option<**String**> |  | [optional]
**released_by_entry_id** | Option<**String**> |  | [optional]
**reference_type** | Option<**String**> |  | [optional]
**reference_id** | Option<**String**> |  | [optional]
**reverses_entry_id** | Option<**String**> |  | [optional]
**cause** | Option<**String**> |  | [optional]
**actor** | Option<**String**> |  | [optional]
**created_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


