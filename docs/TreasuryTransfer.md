# TreasuryTransfer

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**payee_id** | Option<**String**> | 24-character payee id | [optional]
**payee_name** | Option<**String**> | The payee's name when Zernio knows it, for example a creator's display name in one of your creator campaigns; null otherwise | [optional]
**destination_type** | Option<**DestinationType**> |  (enum: creator, ad_account) | [optional]
**amount_cents** | Option<**i32**> | Amount the payee receives, in full | [optional]
**fee_cents** | Option<**i32**> | Zernio fee added on top, 4% with a 50 cent minimum | [optional]
**total_cents** | Option<**i32**> | Amount debited from your balance: amountCents plus feeCents | [optional]
**currency** | Option<**String**> |  | [optional]
**reference** | Option<[**models::TreasuryTransferReference**](TreasuryTransferReference.md)> |  | [optional]
**status** | Option<**Status**> |  (enum: pending, paid, failed, reversed) | [optional]
**failure_reason** | Option<**String**> |  | [optional]
**created_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


