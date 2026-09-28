# UpdateBrandedCallingIdentityRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**display_name** | Option<**String**> | Shown on the callee's screen. No emoji. | [optional]
**call_reasons** | Option<**Vec<String>**> | 1 to 10 reasons you call, each up to 64 characters. Pick from GET /v1/branded-calling/call-reasons to skip manual vetting. | [optional]
**logo_url** | Option<**String**> | HTTPS URL of a PNG, JPEG, WebP or SVG logo. Zernio converts it to the 256x256 BMP the carriers require and hosts it. | [optional]
**authorizer** | Option<[**models::CreateBrandedCallingIdentityRequestAuthorizer**](CreateBrandedCallingIdentityRequestAuthorizer.md)> |  | [optional]
**references** | Option<[**models::BrandedCallingReferences**](BrandedCallingReferences.md)> |  | [optional]
**review_answers** | Option<[**std::collections::HashMap<String, models::UpdateBrandedCallingIdentityRequestReviewAnswersValue>**](UpdateBrandedCallingIdentityRequestReviewAnswersValue.md)> | One entry per point id of the open reviewRequest. A text point takes text; a link point takes url; file and link_or_file points take url set to the URL of a file you uploaded first (POST /v1/media/upload). A point id that is not on the open request is a 422. | [optional]
**review_note** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


