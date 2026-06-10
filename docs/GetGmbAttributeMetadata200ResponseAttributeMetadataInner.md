# GetGmbAttributeMetadata200ResponseAttributeMetadataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**parent** | Option<**String**> | Resource name of the attribute (e.g. \"attributes/has_delivery\"). | [optional]
**value_type** | Option<**String**> | Value type (e.g. BOOL, ENUM, URL, REPEATED_ENUM). | [optional]
**display_name** | Option<**String**> | Localized human-readable attribute name. | [optional]
**group_display_name** | Option<**String**> | Display name of the attribute group. | [optional]
**repeatable** | Option<**bool**> | True if multiple values can be set simultaneously. | [optional]
**deprecated** | Option<**bool**> | True if this attribute should no longer be used. | [optional]
**value_metadata** | Option<[**Vec<models::GetGmbAttributeMetadata200ResponseAttributeMetadataInnerValueMetadataInner>**](GetGmbAttributeMetadata200ResponseAttributeMetadataInnerValueMetadataInner.md)> | Possible enum values (for ENUM / REPEATED_ENUM types). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


