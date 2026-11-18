# TrackingSiteProxy

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**path** | Option<**String**> | Such as `/zt`: the snippet loads `https://<first domain>/zt/z.js`. | [optional]
**secret** | Option<**String**> | Signs the visitor's IP and country your proxy forwards. Only on reading or updating one site. | [optional]
**google_tags** | Option<[**Vec<models::TrackingSiteProxyGoogleTagsInner>**](TrackingSiteProxyGoogleTagsInner.md)> | The loader of each of `googleTagIds` on the site's own domain. Use `src` in place of the tag's googletagmanager.com address. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


