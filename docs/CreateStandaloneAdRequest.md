# CreateStandaloneAdRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**ad_account_id** | **String** |  | 
**name** | **String** |  | 
**goal** | **Goal** | Available goals vary by platform. Meta (Facebook/Instagram) and TikTok support all 7. LinkedIn supports all except app_promotion. Twitter/X supports engagement, traffic, awareness, video_views, app_promotion. Pinterest and Google Ads support only engagement, traffic, awareness, video_views. (enum: engagement, traffic, awareness, video_views, lead_generation, conversions, app_promotion) | 
**budget_amount** | **f64** |  | 
**budget_type** | **BudgetType** |  (enum: daily, lifetime) | 
**currency** | Option<**String**> |  | [optional]
**headline** | Option<**String**> | Required for most platforms. Max: Meta=255, Google=30, Pinterest=100 | [optional]
**long_headline** | Option<**String**> | Google Display only | [optional]
**body** | **String** | Max: Google=90, Pinterest=500 | 
**call_to_action** | Option<**CallToAction**> | Meta only (enum: LEARN_MORE, SHOP_NOW, SIGN_UP, BOOK_TRAVEL, CONTACT_US, DOWNLOAD, GET_OFFER, GET_QUOTE, SUBSCRIBE, WATCH_MORE) | [optional]
**link_url** | Option<**String**> |  | [optional]
**image_url** | Option<**String**> | Image URL (or video URL for TikTok). Not required for Google Search campaigns. | [optional]
**business_name** | Option<**String**> | Google Display only | [optional]
**board_id** | Option<**String**> | Pinterest only. Board ID (auto-creates if not provided). | [optional]
**countries** | Option<**Vec<String>**> |  | [optional]
**age_min** | Option<**i32**> |  | [optional]
**age_max** | Option<**i32**> |  | [optional]
**interests** | Option<[**Vec<models::UpdateAdRequestTargetingInterestsInner>**](UpdateAdRequestTargetingInterestsInner.md)> | Interest objects from /v1/ads/interests. Each must include id and name. | [optional]
**end_date** | Option<**String**> | Required for lifetime budgets | [optional]
**audience_id** | Option<**String**> | Custom audience ID for targeting | [optional]
**campaign_type** | Option<**CampaignType**> | Google only (enum: display, search) | [optional][default to Display]
**keywords** | Option<**Vec<String>**> | Google Search only | [optional]
**additional_headlines** | Option<**Vec<String>**> | Google Search RSA only. Extra headlines. | [optional]
**additional_descriptions** | Option<**Vec<String>**> | Google Search RSA only. Extra descriptions. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


