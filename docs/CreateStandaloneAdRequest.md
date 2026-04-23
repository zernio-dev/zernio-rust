# CreateStandaloneAdRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**ad_account_id** | **String** |  | 
**name** | **String** |  | 
**goal** | Option<**Goal**> | Required on legacy + multi-creative shapes. Inherited from the ad set on the attach shape. Available goals vary by platform. (enum: engagement, traffic, awareness, video_views, lead_generation, conversions, app_promotion) | [optional]
**budget_amount** | Option<**f64**> | Required on legacy + multi-creative shapes. Inherited on attach. | [optional]
**budget_type** | Option<**BudgetType**> | Required on legacy + multi-creative shapes. Inherited on attach. (enum: daily, lifetime) | [optional]
**currency** | Option<**String**> |  | [optional]
**headline** | Option<**String**> | Required for Meta, Google, and Pinterest on legacy + attach shapes (skip for multi-creative — use `creatives[].headline`). Ignored for TikTok and X/Twitter. Max: Meta=255, Google=30, Pinterest=100. | [optional]
**long_headline** | Option<**String**> | Google Display only. Defaults to `headline` if omitted. | [optional]
**body** | Option<**String**> | Required on legacy + attach shapes. For X/Twitter this is the tweet text (max 280 chars including a ~24-char URL when `linkUrl` is set). Max: Google=90, Pinterest=500. | [optional]
**call_to_action** | Option<**CallToAction**> | Required on legacy + attach shapes. Meta only. (enum: LEARN_MORE, SHOP_NOW, SIGN_UP, BOOK_TRAVEL, CONTACT_US, DOWNLOAD, GET_OFFER, GET_QUOTE, SUBSCRIBE, WATCH_MORE) | [optional]
**link_url** | Option<**String**> | Required on legacy + attach shapes. Skip for multi-creative. | [optional]
**image_url** | Option<**String**> | Image creative for Meta/Google/Pinterest on legacy + attach shapes (mutually exclusive with `video`). Not required for Google Search campaigns. For TikTok, this field carries the VIDEO URL (the TikTok ads endpoint is video-only; the field retains the `imageUrl` name for cross-platform consistency). Ignored for X/Twitter. For Google Display, treated as the landscape image (alias of `images.landscape`); supply `images.square` alongside or the request is rejected. | [optional]
**images** | Option<[**models::CreateStandaloneAdRequestImages**](CreateStandaloneAdRequestImages.md)> |  | [optional]
**video** | Option<[**models::CreateStandaloneAdRequestVideo**](CreateStandaloneAdRequestVideo.md)> |  | [optional]
**creatives** | Option<[**Vec<models::CreateStandaloneAdRequestCreativesInner>**](CreateStandaloneAdRequestCreativesInner.md)> | Meta-only. When present, switches to the multi-creative shape: creates 1 campaign + 1 ad set + N ads (one per entry here). Top-level `headline` / `body` / `imageUrl` / `linkUrl` / `callToAction` are ignored in this mode. Mutually exclusive with `adSetId`.  | [optional]
**ad_set_id** | Option<**String**> | Meta-only. When present, switches to the attach shape: adds one new ad to this existing ad set without creating a new campaign. Budget, targeting, goal, and schedule are inherited from the ad set on Meta. Mutually exclusive with `creatives[]`.  | [optional]
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
**advantage_audience** | Option<**AdvantageAudience**> | Meta only. Controls the Advantage audience feature (targeting_automation). 0 = disabled (default), 1 = enabled. Meta Marketing API requires this field on all ad set creation requests. (enum: 0, 1) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


