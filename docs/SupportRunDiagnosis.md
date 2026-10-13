# SupportRunDiagnosis

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**category** | **Category** | What kind of problem the answer describes. New values may be added: treat any value you do not recognize as `other`. (enum: account_connection, content_rejected, rate_limited, platform_issue, zernio_issue, billing, configuration, how_to, other) | 
**cause** | Option<**String**> | The cause the answer gives, in one sentence. Null when the answer reports no problem, for example a how-to question. | 
**fix_steps** | **Vec<String>** | The steps the answer recommends, in order. Empty when it recommends none. | 
**docs_links** | **Vec<String>** | Links to docs.zernio.com that the answer itself cites. Empty when it cites none. | 
**who_must_act** | **WhoMustAct** | Who has to act to resolve it: you (`integrator`), your end user, Zernio, the social platform, or nobody. New values may be added: treat any value you do not recognize as `none`. (enum: integrator, end_user, zernio, platform, none) | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


