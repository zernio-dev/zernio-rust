# InstallTrackingTagOnStore200ResponseInstall

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**store_account_id** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: shopify, wordpress) | [optional]
**installed** | Option<**bool**> | Shopify: this tag is the pixel the store fires. WordPress: the Zernio widget for this tag is in an active widget area with its script intact. | [optional]
**shop_domain** | Option<**String**> | Shopify only. | [optional]
**installed_tag_id** | Option<**String**> | Shopify only: the Meta pixel the store fires now (may be a different tag), or null. | [optional]
**web_pixel_id** | Option<**String**> | Shopify only: web pixel id, or null when nothing is installed. | [optional]
**site_url** | Option<**String**> | WordPress only. | [optional]
**method** | Option<**Method**> | WordPress only. (enum: wordpress_widget) | [optional]
**widget_id** | Option<**String**> | WordPress only: widget id, e.g. `custom_html-3`. | [optional]
**sidebar_id** | Option<**String**> | WordPress only: widget area holding the widget. | [optional]
**replaced_tag_id** | Option<**String**> | Shopify only: the pixel this install replaced on the store, if any. | [optional]
**sidebar_name** | Option<**String**> | WordPress only: name of the widget area used. | [optional]
**created** | Option<**bool**> | WordPress only: false when an existing Zernio widget was updated. | [optional]
**homepage_check** | Option<**HomepageCheck**> | WordPress only: whether the pixel appeared in the homepage HTML. `not_found` can be a stale page cache. (enum: found, not_found, unreachable, skipped) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


