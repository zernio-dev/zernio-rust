# CampaignParticipant

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**campaign_id** | **String** |  | 
**creator** | [**models::CampaignParticipantCreator**](CampaignParticipantCreator.md) |  | 
**status** | **Status** |  (enum: invited, active, suspended, removed) | 
**joined_at** | Option<**String**> |  | 
**accounts** | [**Vec<models::CampaignParticipantAccountsInner>**](CampaignParticipantAccountsInner.md) | Social accounts the creator connected, verified once Zernio confirmed the creator owns them. | 
**balances** | [**models::CampaignParticipantBalances**](CampaignParticipantBalances.md) |  | 
**flags** | [**Vec<models::CampaignParticipantFlagsInner>**](CampaignParticipantFlagsInner.md) |  | 
**submission_counts** | [**models::CampaignSubmissionCounts**](CampaignSubmissionCounts.md) |  | 
**payout** | [**models::CampaignParticipantPayout**](CampaignParticipantPayout.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


