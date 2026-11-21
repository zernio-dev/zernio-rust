# EditCampaignNegativeKeywordsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | Option<**Platform**> | Optional and NOT authoritative: the resolved campaign's own platform decides 200 vs 501, never this hint. (enum: facebook, instagram, tiktok, linkedin, pinterest, google, twitter, openai, reddit) | [optional]
**add** | Option<[**Vec<models::KeywordEntry>**](KeywordEntry.md)> | Negative keywords to add. Send at least one entry in add or remove. | [optional]
**remove** | Option<[**Vec<models::KeywordEntry>**](KeywordEntry.md)> | Negative keywords to remove. Bare strings mean broad match. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


