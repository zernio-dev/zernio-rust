# RcsAgent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**profile_id** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> | The rcs inbox account, created once the agent exists with the carriers. | [optional]
**country** | Option<**String**> | Launch market (ISO 3166-1 alpha-2). US agents run through the carriers automatically; other markets are filed by our team and skip the testing and launch_review steps (send the launch request while the agent is still in review). | [optional]
**status** | Option<**Status**> |  (enum: requested, changes_requested, brand_vetting, agent_review, testing, launch_review, launching, live, rejected, deactivated) | [optional]
**display_name** | Option<**String**> |  | [optional]
**use_case** | Option<**UseCase**> |  (enum: MULTI_USE, PROMOTIONAL, TRANSACTIONAL, OTP) | [optional]
**profile** | Option<[**models::RcsAgentProfile**](RcsAgentProfile.md)> |  | [optional]
**brand** | Option<[**models::RcsBrand**](RcsBrand.md)> |  | [optional]
**launch_request** | Option<[**models::RcsLaunchRequest**](RcsLaunchRequest.md)> |  | [optional]
**carrier_approvals** | Option<[**Vec<models::RcsCarrierApproval>**](RcsCarrierApproval.md)> |  | [optional]
**test_devices** | Option<[**Vec<models::RcsTestDevice>**](RcsTestDevice.md)> |  | [optional]
**sms_fallback_from** | Option<**String**> |  | [optional]
**review_note** | Option<**String**> | Our note while status is changes_requested. | [optional]
**decline_reason** | Option<**String**> |  | [optional]
**requested_at** | Option<**String**> |  | [optional]
**submitted_at** | Option<**String**> |  | [optional]
**live_at** | Option<**String**> |  | [optional]
**created_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


