# CreateStandaloneAdRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**ad_account_id** | **String** |  | 
**name** | **String** |  | 
**goal** | **Goal** |  (enum: engagement, traffic, awareness, video_views) | 
**budget_amount** | **f64** |  | 
**budget_type** | **BudgetType** |  (enum: daily, lifetime) | 
**currency** | Option<**String**> |  | [optional]
**headline** | Option<**String**> | Required for most platforms. Max: Meta=255, Google=30, Pinterest=100 | [optional]
**body** | **String** | Max: Google=90, Pinterest=500 | 
**call_to_action** | Option<**CallToAction**> | Meta only (enum: LEARN_MORE, SHOP_NOW, SIGN_UP, BOOK_TRAVEL, CONTACT_US, DOWNLOAD, GET_OFFER, GET_QUOTE, SUBSCRIBE, WATCH_MORE) | [optional]
**link_url** | Option<**String**> |  | [optional]
**image_url** | **String** | Image URL (or video URL for TikTok) | 
**countries** | Option<**Vec<String>**> |  | [optional]
**age_min** | Option<**i32**> |  | [optional]
**age_max** | Option<**i32**> |  | [optional]
**interests** | Option<**Vec<String>**> |  | [optional]
**end_date** | Option<**String**> | Required for lifetime budgets | [optional]
**audience_id** | Option<**String**> | Custom audience ID for targeting | [optional]
**campaign_type** | Option<**CampaignType**> | Google only (enum: display, search) | [optional][default to Display]
**keywords** | Option<**Vec<String>**> | Google Search only | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


