# CreateStandaloneAdRequestCarouselCardsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**image_url** | Option<**String**> | Image card: the card image, uploaded to the ad account and referenced by hash. | [optional]
**video** | Option<[**models::CreateStandaloneAdRequestCarouselCardsInnerVideo**](CreateStandaloneAdRequestCarouselCardsInnerVideo.md)> |  | [optional]
**link_url** | Option<**String**> | Card destination URL. Defaults to the top-level linkUrl, or Meta's lead-form link when leadGenFormId is set and neither is provided. | [optional]
**headline** | Option<**String**> | Card headline, shown below the card image. | [optional]
**description** | Option<**String**> | Card description, shown under the headline. | [optional]
**call_to_action** | Option<**String**> | Card CTA override. Defaults to the top-level callToAction; same enum. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


