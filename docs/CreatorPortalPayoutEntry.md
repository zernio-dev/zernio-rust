# CreatorPortalPayoutEntry

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**kind** | **Kind** |  (enum: accrual, approval, hold_release, adjustment, settling, settlement, reversal, topup, transfer, fee) | 
**amount_cents** | **i32** |  | 
**from_bucket** | Option<**String**> | The participant bucket the money left; null when it came from outside the participant. | 
**to_bucket** | Option<**String**> | The participant bucket the money entered; null when it left the participant. | 
**hold_until** | Option<**String**> |  | 
**created_at** | **String** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


