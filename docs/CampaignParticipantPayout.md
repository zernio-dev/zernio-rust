# CampaignParticipantPayout

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **Status** | `not_started`: no payout account yet. `onboarding`: setup started or under review. `ready`: payouts enabled. `restricted`: Stripe needs more information before paying out. (enum: not_started, onboarding, ready, restricted) | 
**country** | Option<**String**> | ISO 3166-1 alpha-2 country of the payout account, null before setup starts. Zernio pays out only to the US, Canada, the UK, the EEA, Switzerland and Gibraltar; pay creators elsewhere yourself and record it with `recordOnly: true`. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


