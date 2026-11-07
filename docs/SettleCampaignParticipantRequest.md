# SettleCampaignParticipantRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount_cents** | Option<**i32**> | Defaults to the whole payable balance. | [optional]
**external_reference** | Option<**String**> | Your payout id. Required when the campaign settles externally. | [optional]
**record_only** | Option<**bool**> | Treasury campaigns only, and required there: record a payout you already made outside Zernio. Ignored on other settlement modes, which always record. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


