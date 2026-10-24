# UpdateFacebookPageInfoRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**about** | Option<**String**> | Short description, shown as Description in the Page's Edit Page Info. | [optional]
**description** | Option<**String**> | Longer text, shown as Additional Information. | [optional]
**website** | Option<**String**> | URL of the Page's website. | [optional]
**phone** | Option<**String**> |  | [optional]
**emails** | Option<**Vec<String>**> | Replaces every email listed on the Page. | [optional]
**hours** | Option<**std::collections::HashMap<String, String>**> | Replaces the opening hours. Keys are `{day}_{slot}_{open|close}` with day `mon` to `sun` and slot 1 or 2, values are 24h `HH:MM` times. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


