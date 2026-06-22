# CreateLeadFormRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**name** | **String** |  | 
**questions** | [**Vec<models::CreateLeadFormRequestQuestionsInner>**](CreateLeadFormRequestQuestionsInner.md) |  | 
**privacy_policy_url** | **String** |  | 
**privacy_policy_link_text** | Option<**String**> |  | [optional]
**follow_up_action_url** | Option<**String**> |  | [optional]
**locale** | Option<**String**> |  | [optional]
**thank_you_title** | Option<**String**> |  | [optional]
**thank_you_body** | Option<**String**> |  | [optional]
**thank_you_button_text** | Option<**String**> |  | [optional]
**thank_you_button_type** | Option<**String**> |  | [optional]
**thank_you_website_url** | Option<**String**> |  | [optional]
**is_optimized_for_quality** | Option<**bool**> | Legacy form type toggle. Prefer formType instead. false = More Volume, true = Higher Intent. | [optional]
**form_type** | Option<**FormType**> | Form type. MORE_VOLUME = optimized for lead quantity (default). HIGHER_INTENT = adds a review/confirmation step before submit. RICH_CREATIVE = includes context card and custom headline to educate users before they submit. Supersedes isOptimizedForQuality. (enum: MORE_VOLUME, HIGHER_INTENT, RICH_CREATIVE) | [optional]
**block_display_for_non_targeted_viewer** | Option<**bool**> | Sharing setting. true = Restricted (only people targeted by the ad can open the form link). false = Open (shareable link, default). | [optional]
**allow_organic_lead_gen** | Option<**bool**> | Flexible form delivery. true = the form can surface organically on the Page (not just as a paid ad). Defaults to false. | [optional]
**question_page_custom_headline** | Option<**String**> | Custom subheadline shown above the form fields on the questions page (the contact-information section description). Defaults to Meta's generic copy when omitted. | [optional]
**context_card** | Option<[**models::CreateLeadFormRequestContextCard**](CreateLeadFormRequestContextCard.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


