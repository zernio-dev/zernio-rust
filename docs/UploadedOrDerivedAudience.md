# UploadedOrDerivedAudience

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**ad_account_id** | **String** | Platform ad account ID. Must start with act_ for Meta; bare platform id for others (Google customer id, X/TikTok/LinkedIn/Pinterest account id). | 
**name** | **String** |  | 
**description** | Option<**String**> |  | [optional]
**r#type** | **Type** |  (enum: customer_list, company_list, engagement, meta_engagement, website, website_retargeting, lookalike) | 
**match_rules** | Option<[**Vec<models::UploadedOrDerivedAudienceMatchRulesInner>**](UploadedOrDerivedAudienceMatchRulesInner.md)> | Required for website_retargeting audiences (LinkedIn only). Each rule is a URL pattern; a member who visits any matching page enters the segment. Needs the LinkedIn Insight Tag installed on the customer's site — the segment only starts filling once the tag reports visits.  The response's `platformAudienceId` is the LinkedIn adSegment id, valid for downstream use. These segments appear in GET /v1/ads/audiences with  `type: website_retargeting` once LinkedIn has finished building them.  | [optional]
**source_type** | Option<**SourceType**> | Required for engagement audiences (LinkedIn only): what members engaged with — a video/leadgen/single-image ad campaign, a Company Page or an Event page.  (enum: VIDEO_ADS, LEAD_GEN_FORMS, ORGANIZATION_PAGES, EVENT_PAGES, SINGLE_IMAGE_ADS) | [optional]
**trigger** | Option<**String**> | Required for engagement audiences. The action, validated by LinkedIn against `sourceType`. Common values: VIDEO_ADS FIRST_QUARTILE / MIDPOINT / THIRD_QUARTILE / FULL_COMPLETE; LEAD_GEN_FORMS VIEW_FORM / LEAD_FORM_SUBMIT; ORGANIZATION_PAGES VIEW / CTA_CLICK; EVENT_PAGES RSVPED / VIDEO_VIEWED / ENGAGEMENT / CLICK.  | [optional]
**lookback_days** | Option<**LookbackDays**> | Required for engagement audiences. Rolling window. (enum: 30, 60, 90, 180, 365) | [optional]
**engagement_sources** | Option<**Vec<String>**> | Required for engagement audiences. Campaign URNs for the ad source types, organization URNs for pages and events. LinkedIn creates one rule per source, all sharing the same trigger and lookbackDays.  | [optional]
**companies** | Option<[**Vec<models::UploadedOrDerivedAudienceCompaniesInner>**](UploadedOrDerivedAudienceCompaniesInner.md)> | Required for company_list audiences (LinkedIn only): plain-text company rows for account targeting. Each row needs at least one identifier. Not hashed, LinkedIn matches these against its own company graph. LinkedIn recommends 1,000+ companies for a usable match rate and takes up to 48h to process the list. Replace the list later with POST /v1/ads/audiences/{audienceId}/companies.  | [optional]
**pixel_id** | Option<**String**> | Required for website audiences | [optional]
**retention_days** | Option<**i32**> | Required for website (max 180) and meta_engagement (max 365) audiences. | [optional]
**engagement_source** | Option<**EngagementSource**> | Required for meta_engagement audiences (Meta only): what people engaged with. `page` = a Facebook Page, `instagram` = an IG professional account, `video` = a video. The source object must be eligible for engagement audiences or Meta rejects with subcode 1713151 (\"Invalid Event Name\"), surfaced verbatim.  (enum: page, instagram, video) | [optional]
**source_id** | Option<**String**> | Required for meta_engagement: the Page / IG account / video id. | [optional]
**event** | Option<**String**> | meta_engagement only. The engagement event; defaults per source (page → page_engaged, instagram → ig_business_profile_all, video → video_watched). Ignored when `rule` is provided.  | [optional]
**source_audience_id** | Option<**String**> | Required for lookalike audiences | [optional]
**country** | Option<**String**> | 2-letter code, required for lookalike audiences | [optional]
**ratio** | Option<**f64**> | Required for lookalike audiences | [optional]
**url_contains** | Option<**String**> | website only. Narrows the audience from all visitors to visitors of URLs containing this substring. Ignored when `rule` is supplied.  | [optional]
**rule** | Option<**serde_json::Value**> | Optional raw Meta rule, replacing the one we build. Omit it for all visitors of `pixelId`, or use `urlContains` for the common page-match case.  For `website` this is Meta's Flexible Audience Rule and is VALIDATED before we call Meta: every entry in `inclusions.rules` (and `exclusions.rules`) must carry `event_sources`, `retention_seconds` AND `filter`. Meta rejects a rule missing any of the three with code 100 / subcode 1713098 (\"Invalid rule JSON format\"), so a bad shape is a 400 here instead. The pre-2018 flat shapes (`{url: ...}`, `{event: ...}`) are not accepted by Meta at all (subcode 1870029).  Example, visitors of /checkout in the last 30 days: `{\"inclusions\":{\"operator\":\"or\",\"rules\":[{\"event_sources\":[{\"id\":\"<pixelId>\",\"type\":\"pixel\"}],\"retention_seconds\":2592000,\"filter\":{\"operator\":\"and\",\"filters\":[{\"field\":\"url\",\"operator\":\"i_contains\",\"value\":\"/checkout\"}]}}]}}`  Note Meta DERIVES `retention_days` from `retention_seconds` and stores `event_sources[].id` as a number, so a rule read back will not be byte-identical to the one you sent.  For `meta_engagement` the rule is forwarded verbatim and NOT validated: that type has two dialects (the `video` source uses a legacy flat array), so no single schema covers both.  | [optional]
**customer_file_source** | Option<**String**> | Data source declaration for GDPR compliance (customer_list only) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


