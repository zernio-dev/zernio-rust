# BusinessAgentWebsite

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **String** |  | 
**included_sub_domains** | Option<**Vec<String>**> |  | [optional]
**included_url_patterns** | Option<**Vec<String>**> | Only URLs containing one of these substrings are ingested. | [optional]
**excluded_sub_domains** | Option<**Vec<String>**> |  | [optional]
**excluded_url_patterns** | Option<**Vec<String>**> |  | [optional]
**single_urls** | Option<**Vec<String>**> | Crawl only these exact pages instead of the whole site. | [optional]
**id** | **String** |  | 
**crawl_status** | Option<**String**> | not_started, pending, in_progress, completed, completed_no_data or failed (see crawl_error). | [optional]
**crawl_error** | Option<**String**> |  | [optional]
**pages_crawled** | Option<**i32**> |  | [optional]
**last_crawled_at** | Option<**i32**> | Unix seconds. | [optional]
**created_at** | Option<**i32**> | Unix seconds. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


