# CreateStandaloneAd200ResponseResultsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**node** | Option<**Node**> |  (enum: campaign, adSet, creative, ad, performanceMaxCampaign) | [optional]
**status** | Option<**Status**> |  (enum: validated, skipped) | [optional]
**reason** | Option<**String**> | Why the node could not be validated (on skipped), or what the dry run could not check and what the request would do as sent (on validated). A Performance Max validation with no location targeting reports here that the campaign would run worldwide. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


