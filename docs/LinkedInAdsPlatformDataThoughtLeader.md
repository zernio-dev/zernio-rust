# LinkedInAdsPlatformDataThoughtLeader

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**post_urn** | **String** | LinkedIn share or ugcPost URN, urn:li:share:N or urn:li:ugcPost:N. Get it via \"Copy link to post\" on the target LinkedIn post (the URL contains -share- for a share or -ugcPost- for a ugcPost, then the numeric id). The post must be authored by an organization (Company Page). Member (personal profile) posts, i.e. Thought Leader Ads proper, are rejected by LinkedIn's public Marketing API regardless of sponsorship approval and of post type (a LinkedIn limitation; their Campaign Manager creates those through a private API). Referencing a member post returns a 422 with a clear error.  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


