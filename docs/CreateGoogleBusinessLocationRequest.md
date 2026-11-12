# CreateGoogleBusinessLocationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **String** | Business name as shown on Google. | 
**language_code** | **String** | BCP-47 language of the listing (e.g. \"es\"). Immutable after creation. | 
**primary_category** | **String** | Category name from GET gmb-categories (e.g. \"categories/gcid:cafe\"). A bare \"gcid:cafe\" is also accepted. | 
**additional_categories** | Option<**Vec<String>**> | Further category names, same format as primaryCategory. | [optional]
**storefront_address** | Option<[**models::CreateGoogleBusinessLocationRequestStorefrontAddress**](CreateGoogleBusinessLocationRequestStorefrontAddress.md)> |  | [optional]
**service_area** | Option<[**models::CreateGoogleBusinessLocationRequestServiceArea**](CreateGoogleBusinessLocationRequestServiceArea.md)> |  | [optional]
**phone** | Option<**String**> | Primary phone number. Required when storefrontAddress is absent and websiteUri is not set. | [optional]
**website_uri** | Option<**String**> | Website URL. Required when storefrontAddress is absent and phone is not set. | [optional]
**description** | Option<**String**> | Business description (Google profile.description). | [optional]
**regular_hours** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Google `regularHours` object (periods with openDay, openTime, closeDay, closeTime). | [optional]
**validate_only** | Option<**bool**> | Validate with Google without creating the listing or attaching anything. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


