# GetAd200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad** | Option<[**models::Ad**](Ad.md)> |  | [optional]
**cached_at** | Option<**String**> | Google RSA details cache timestamp. | [optional]
**stale** | Option<**bool**> | Whether Google RSA details use the last successful cached response. | [optional]
**status_read_at** | Option<**String**> | With `live=true`, when the switches were read from the platform; null when the live read failed and the stored values were returned. Always set on an unsynced Meta ad read with `accountId`, the time of that read. | [optional]
**dark_post** | Option<[**models::GetAd200ResponseDarkPost**](GetAd200ResponseDarkPost.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


