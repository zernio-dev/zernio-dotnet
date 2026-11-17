# Zernio.Model.TrackingSiteProxy
The path your server forwards to the collector, so the tag runs from the site's own domain. Null when it has none.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Path** | **string** | Such as &#x60;/zt&#x60;: the snippet loads &#x60;https://&lt;first domain&gt;/zt/z.js&#x60;. | [optional] 
**Secret** | **string** | Signs the visitor&#39;s IP and country your proxy forwards. Only on reading or updating one site. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

