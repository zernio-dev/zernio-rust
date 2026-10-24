# FacebookPageInfo

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**about** | Option<**String**> | Short description, shown as Description in the Page's Edit Page Info. | 
**description** | Option<**String**> | Longer text, shown as Additional Information. | 
**website** | Option<**String**> |  | 
**phone** | Option<**String**> |  | 
**emails** | **Vec<String>** |  | 
**hours** | **std::collections::HashMap<String, String>** | Opening hours keyed `{day}_{slot}_{open|close}`, for example `mon_1_open: \"09:00\"`. Empty when the Page has none. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


