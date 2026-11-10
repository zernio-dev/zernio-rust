# CreatorPortalParticipant

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**kind** | **Kind** |  (enum: participant) | 
**campaign** | [**models::CreatorPortalCampaign**](CreatorPortalCampaign.md) |  | 
**participant** | [**models::CreatorPortalParticipantParticipant**](CreatorPortalParticipantParticipant.md) |  | 
**accounts** | [**Vec<models::CreatorPortalParticipantAccountsInner>**](CreatorPortalParticipantAccountsInner.md) | Verified accounts on the campaign's platforms. | 
**submissions** | [**Vec<models::CreatorPortalSubmission>**](CreatorPortalSubmission.md) | The latest 100 submissions. | 
**drafts** | [**Vec<models::CreatorPortalDraft>**](CreatorPortalDraft.md) | The latest 100 draft versions, newest first. Empty on a campaign that does not review drafts. | 
**samples** | [**Vec<models::CreatorPortalSample>**](CreatorPortalSample.md) | Every sample request of the creator, newest first. | 
**earnings** | [**models::CreatorPortalParticipantEarnings**](CreatorPortalParticipantEarnings.md) |  | 
**payouts** | [**models::CreatorPortalPayoutSetup**](CreatorPortalPayoutSetup.md) |  | 
**referral** | Option<[**models::CreatorPortalReferral**](CreatorPortalReferral.md)> |  | [optional]
**retainer** | Option<[**models::CreatorPortalParticipantRetainer**](CreatorPortalParticipantRetainer.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


