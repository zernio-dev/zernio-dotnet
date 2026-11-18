# Zernio.Model.UpdateTrackingSiteRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | [optional] 
**Domains** | **List&lt;string&gt;** | Hosts allowed to send events, such as &#x60;brand.com&#x60;. Events from any other origin are dropped. | [optional] 
**ConsentMode** | **TrackingSiteConsentMode** |  | [optional] 
**CustomHostname** | **string** | A subdomain of one of the site&#39;s domains, never the domain itself. &#x60;null&#x60; removes it. | [optional] 
**ProxyPath** | **string** | The path your server forwards to the collector, such as &#x60;/zt&#x60;. &#x60;null&#x60; removes it. | [optional] 
**GoogleTagIds** | **List&lt;string&gt;** | Google tag ids such as &#x60;GTM-XXXXXXX&#x60;, &#x60;G-XXXXXXXXXX&#x60; or &#x60;AW-XXXXXXXXXX&#x60;, up to 10. &#x60;null&#x60; or &#x60;[]&#x60; removes them. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

