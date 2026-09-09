# UpdateGoogleBusinessLocationDetailsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**update_mask** | **String** | Required. Comma-separated fields to update (e.g. 'regularHours', 'specialHours', 'profile.description', 'categories', 'serviceItems'). Any valid Google Business Information API updateMask field is supported. | 
**regular_hours** | Option<[**models::UpdateGoogleBusinessLocationDetailsRequestRegularHours**](UpdateGoogleBusinessLocationDetailsRequestRegularHours.md)> |  | [optional]
**special_hours** | Option<[**models::GetGoogleBusinessLocationDetails200ResponseSpecialHours**](GetGoogleBusinessLocationDetails200ResponseSpecialHours.md)> |  | [optional]
**profile** | Option<[**models::UpdateGoogleBusinessLocationDetailsRequestProfile**](UpdateGoogleBusinessLocationDetailsRequestProfile.md)> |  | [optional]
**website_uri** | Option<**String**> |  | [optional]
**phone_numbers** | Option<[**models::GetGoogleBusinessLocationDetails200ResponsePhoneNumbers**](GetGoogleBusinessLocationDetails200ResponsePhoneNumbers.md)> |  | [optional]
**categories** | Option<[**models::UpdateGoogleBusinessLocationDetailsRequestCategories**](UpdateGoogleBusinessLocationDetailsRequestCategories.md)> |  | [optional]
**service_items** | Option<[**Vec<models::UpdateGoogleBusinessLocationDetailsRequestServiceItemsInner>**](UpdateGoogleBusinessLocationDetailsRequestServiceItemsInner.md)> | Services offered by the business. Use updateMask='serviceItems' to update. | [optional]
**title** | Option<**String**> | Business name. Use updateMask='title'. | [optional]
**store_code** | Option<**String**> | External store identifier, unique within the account. Use updateMask='storeCode'. | [optional]
**labels** | Option<**Vec<String>**> | Free-form, internal-only labels for grouping (1-255 characters each). Use updateMask='labels'. | [optional]
**storefront_address** | Option<[**models::UpdateGoogleBusinessLocationDetailsRequestStorefrontAddress**](UpdateGoogleBusinessLocationDetailsRequestStorefrontAddress.md)> |  | [optional]
**service_area** | Option<[**models::UpdateGoogleBusinessLocationDetailsRequestServiceArea**](UpdateGoogleBusinessLocationDetailsRequestServiceArea.md)> |  | [optional]
**open_info** | Option<[**models::UpdateGoogleBusinessLocationDetailsRequestOpenInfo**](UpdateGoogleBusinessLocationDetailsRequestOpenInfo.md)> |  | [optional]
**more_hours** | Option<[**Vec<models::UpdateGoogleBusinessLocationDetailsRequestMoreHoursInner>**](UpdateGoogleBusinessLocationDetailsRequestMoreHoursInner.md)> | Additional hours for specific services (delivery, drive-through, etc.). Use updateMask='moreHours'. | [optional]
**latlng** | Option<[**models::UpdateGoogleBusinessLocationDetailsRequestLatlng**](UpdateGoogleBusinessLocationDetailsRequestLatlng.md)> |  | [optional]
**ad_words_location_extensions** | Option<[**models::UpdateGoogleBusinessLocationDetailsRequestAdWordsLocationExtensions**](UpdateGoogleBusinessLocationDetailsRequestAdWordsLocationExtensions.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


