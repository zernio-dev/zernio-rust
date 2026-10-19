# GetLinkedInDemographics200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | Option<**bool**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: linkedin) | [optional]
**metric** | Option<**Metric**> |  (enum: follower_demographics) | [optional]
**demographics** | Option<[**std::collections::HashMap<String, Vec<models::GetLinkedInDemographics200ResponseDemographicsValueInner>>**](Vec.md)> | Only the requested breakdowns are present. Entries are sorted by value, largest first. | [optional]
**note** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


