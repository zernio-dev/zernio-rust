# CreatorPortalPayoutSetup

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**mode** | **Mode** | How the campaign pays: treasury means through Zernio, so the creator onboards for payouts, which they can do from the moment they join. Earnings wait until it is done. (enum: none, external, treasury) | 
**status** | **Status** |  (enum: not_started, pending, enabled, not_applicable) | 
**country** | Option<**String**> |  | 
**suggested_country** | Option<**String**> | The country the request came from, to preselect before payout setup starts. Null once the payout account has a country, and outside treasury mode. | 
**transfers** | [**Vec<models::CreatorPortalPayoutSetupTransfersInner>**](CreatorPortalPayoutSetupTransfersInner.md) | Treasury payouts sent to the creator. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


