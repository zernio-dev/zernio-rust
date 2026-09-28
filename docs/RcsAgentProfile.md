# RcsAgentProfile

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**description** | **String** |  | 
**logo_url** | **String** | 224x224, max 50 KB. Upload any image through POST /v1/rcs/assets to get a compliant URL. | 
**hero_url** | **String** | Banner, 1440x448, max 200 KB. Upload through POST /v1/rcs/assets. | 
**brand_color** | **String** | Hex colour, e.g. #1A73E8. Needs 4.5:1 contrast against white. | 
**privacy_policy_url** | **String** |  | 
**terms_url** | **String** |  | 
**phone** | Option<[**models::RcsAgentProfilePhone**](RcsAgentProfilePhone.md)> |  | [optional]
**website** | Option<[**models::RcsAgentProfileWebsite**](RcsAgentProfileWebsite.md)> |  | [optional]
**email** | Option<[**models::RcsAgentProfileEmail**](RcsAgentProfileEmail.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


