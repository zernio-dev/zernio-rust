# CommerceCatalogSync

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> | The store SocialAccount id. | [optional]
**catalog_platform** | Option<**CatalogPlatform**> |  (enum: meta) | [optional]
**catalog_account_id** | Option<**String**> | The Meta login account whose token writes to the catalog. | [optional]
**catalog_id** | Option<**String**> |  | [optional]
**run_status** | Option<**RunStatus**> |  (enum: pending, running, succeeded, failed) | [optional]
**last_run_started_at** | Option<**String**> |  | [optional]
**last_run_finished_at** | Option<**String**> |  | [optional]
**last_error** | Option<**String**> | Why the last run failed, or how many items Meta rejected in a run that otherwise succeeded. Null after a clean run. | [optional]
**items_sent** | Option<**i32**> | Catalog items (one per variant) Meta accepted in the last full run. | [optional]
**items_skipped** | Option<**i32**> | Products the last full run could not list: not published to the online store or without an image. | [optional]
**items_deleted** | Option<**i32**> | Items the last full run removed because the store no longer has them. | [optional]
**created_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


