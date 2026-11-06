# AutomationTemplate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | A team template's id (24 hex characters), or the id of one of Zernio's templates such as `stop_losers`. | 
**name** | **String** |  | 
**description** | **String** |  | 
**publisher** | [**models::AutomationTemplatePublisher**](AutomationTemplatePublisher.md) |  | 
**visibility** | **Visibility** | `team`: your team only. `link`: anyone with the share link can read and install it. `public`: one of Zernio's templates. (enum: team, link, public) | 
**version** | **i32** | Goes up each time the content changes. Renaming or sharing keeps it. | 
**areas** | **Vec<Areas>** | What its automations work on. (enum: ads, events, posts, inbox, comments) | 
**inputs** | [**Vec<models::AutomationTemplateInput>**](AutomationTemplateInput.md) |  | 
**automations** | [**Vec<models::AutomationTemplateAutomation>**](AutomationTemplateAutomation.md) |  | 
**installs** | **i32** | Installs across every team. Always 0 on Zernio's templates. | 
**installed_in_team** | Option<**i32**> | Your team's automations made from it. Absent on shared and Zernio templates. | [optional]
**share** | [**models::AutomationTemplateShare**](AutomationTemplateShare.md) |  | 
**created_by** | Option<**String**> | The user who saved it. Only on your team's templates. | [optional]
**created_at** | Option<**String**> | Absent on Zernio's templates. | [optional]
**updated_at** | Option<**String**> | Absent on Zernio's templates. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


