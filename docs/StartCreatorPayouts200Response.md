# StartCreatorPayouts200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **String** | Stripe-hosted onboarding page. Send the creator here; Stripe returns them to their Zernio creator page when done. Expires after a few minutes, so request it when the creator clicks. | 
**client_secret** | **String** | Account session secret for Stripe's embedded onboarding component. Only usable on Zernio's own creator page; integrations use `url`. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


