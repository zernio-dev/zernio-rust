# CampaignReport

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**spend** | [**models::CampaignReportSpend**](CampaignReportSpend.md) |  | 
**views** | [**models::CampaignReportViews**](CampaignReportViews.md) |  | 
**engagements** | **i32** | The campaign engagement types summed over the same submissions. | 
**submissions** | [**models::CampaignSubmissionCounts**](CampaignSubmissionCounts.md) |  | 
**participants** | [**Vec<models::CampaignReportParticipantsInner>**](CampaignReportParticipantsInner.md) | Top 10 participants by payable, settling and settled cents. | 
**authenticity** | [**Vec<models::CampaignReportAuthenticityInner>**](CampaignReportAuthenticityInner.md) | Authenticity score histogram in ten buckets (0-9 through 90-100). | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


