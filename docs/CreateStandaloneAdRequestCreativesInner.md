# CreateStandaloneAdRequestCreativesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**headline** | **String** |  | 
**body** | **String** |  | 
**image_url** | Option<**String**> | Image creative. Mutually exclusive with `video`. | [optional]
**video** | Option<[**models::CreateStandaloneAdRequestCreativesInnerVideo**](CreateStandaloneAdRequestCreativesInnerVideo.md)> |  | [optional]
**link_url** | **String** |  | 
**call_to_action** | **CallToAction** |  (enum: LEARN_MORE, SHOP_NOW, SIGN_UP, BOOK_TRAVEL, CONTACT_US, DOWNLOAD, GET_OFFER, GET_QUOTE, SUBSCRIBE, WATCH_MORE) | 
**lead_gen_form_id** | Option<**String**> | Per-creative Lead Gen Form ID. Wins over the top-level `leadGenFormId` so each ad in a campaign can A/B a different form. Forces CTA to SIGN_UP. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


