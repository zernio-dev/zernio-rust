# GoogleBusinessPlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**location_id** | Option<**String**> | Target GBP location ID (e.g. \"locations/123456789\"). If omitted, uses the default location. Use GET /v1/accounts/{id}/gmb-locations to list locations. | [optional]
**language_code** | Option<**String**> | BCP 47 language code (e.g. \"en\", \"de\", \"es\"). Auto-detected if omitted. Set explicitly for short or mixed-language posts. | [optional]
**topic_type** | Option<**TopicType**> | Post type. STANDARD is a regular update. EVENT requires the event object. OFFER requires the offer object. Defaults to STANDARD if omitted. (enum: STANDARD, EVENT, OFFER) | [optional][default to Standard]
**call_to_action** | Option<[**models::GoogleBusinessPlatformDataCallToAction**](GoogleBusinessPlatformDataCallToAction.md)> |  | [optional]
**event** | Option<[**models::GoogleBusinessPlatformDataEvent**](GoogleBusinessPlatformDataEvent.md)> |  | [optional]
**offer** | Option<[**models::GoogleBusinessPlatformDataOffer**](GoogleBusinessPlatformDataOffer.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


