# LinkedInPlatformDataAudience

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**countries** | Option<**Vec<String>**> | ISO 3166-1 alpha-2 codes with a built-in LinkedIn geo URN (same list as geoRestriction.countries, merged with it). Other countries and sub-country regions go in geoLocations. | [optional]
**geo_locations** | Option<**Vec<String>**> | LinkedIn geo URNs or ids (urn:li:geo:103644278 or 103644278): countries, states, regions, cities. | [optional]
**interface_locales** | Option<[**Vec<models::LinkedInPlatformDataAudienceInterfaceLocalesInner>**](LinkedInPlatformDataAudienceInterfaceLocalesInner.md)> | Members' LinkedIn interface locale, e.g. { language: es, country: ES }. | [optional]
**industries** | Option<**Vec<String>**> | urn:li:industry:<id> or id. | [optional]
**job_functions** | Option<**Vec<String>**> | urn:li:function:<id> or id. | [optional]
**seniorities** | Option<**Vec<String>**> | urn:li:seniority:<id> or id. | [optional]
**staff_count_ranges** | Option<**Vec<StaffCountRanges>**> | Company size of the member's current employer. (enum: SIZE_1, SIZE_2_TO_10, SIZE_11_TO_50, SIZE_51_TO_200, SIZE_201_TO_500, SIZE_501_TO_1000, SIZE_1001_TO_5000, SIZE_5001_TO_10000, SIZE_10001_OR_MORE) | [optional]
**degrees** | Option<**Vec<String>**> | urn:li:degree:<id> or id (LinkedIn standardized degrees). | [optional]
**fields_of_study** | Option<**Vec<String>**> | urn:li:fieldOfStudy:<id> or id (LinkedIn standardized fields of study). | [optional]
**organizations** | Option<**Vec<String>**> | Schools, as urn:li:organization:<id> or id (LinkedIn's Organization Lookup). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


