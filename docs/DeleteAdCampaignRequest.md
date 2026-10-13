# DeleteAdCampaignRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **Platform** |  (enum: facebook, instagram, tiktok, linkedin, pinterest, google, twitter, openai, reddit) | 
**account_id** | Option<**String**> | Zernio SocialAccount id owning the ad account. Required only to delete an EMPTY campaign (zero ads), which has no local Ad documents to resolve a token from. | [optional]
**ad_account_id** | Option<**String**> | X only, for an EMPTY campaign that was never synced: the X ad account id the campaign belongs to (lowercase letters and digits). The synced campaign's ad account wins when there is one. Also accepted on the query string. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


