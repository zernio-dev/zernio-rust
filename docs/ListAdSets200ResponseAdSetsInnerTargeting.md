# ListAdSets200ResponseAdSetsInnerTargeting

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**include** | Option<**serde_json::Value**> | LinkedIn `targetingCriteria.include`, verbatim (an `and` of `or` facet clauses). | [optional]
**exclude** | Option<**serde_json::Value**> | LinkedIn `targetingCriteria.exclude`, verbatim. Absent when the campaign excludes nothing. | [optional]
**audience_expansion_enabled** | Option<**bool**> | LinkedIn audience expansion: whether LinkedIn may also serve to members similar to the criteria. | [optional]
**offsite_delivery_enabled** | Option<**bool**> | Whether the campaign may deliver on the LinkedIn Audience Network, off LinkedIn itself. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


