# Zernio.Model.AdLeadAttribution
`web` leads only: where the lead came from. Its stage events (`QualifiedLead`, `Purchase`) carry these so the ad platforms can match them. Null for ad network leads.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ClickIds** | **Dictionary&lt;string, string&gt;** | Ad click and browser ids of the visit (&#x60;fbc&#x60;, &#x60;fbp&#x60;, &#x60;gclid&#x60;, &#x60;ttclid&#x60;, ...). | [optional] 
**Utm** | **Dictionary&lt;string, string&gt;** |  | [optional] 
**VisitorId** | **string** | The Zernio tag visitor id (&#x60;_zid&#x60;). | [optional] 
**SourceUrl** | **string** | The page the form was submitted on. | [optional] 
**SiteId** | **string** | The tracked website, for a website form lead. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

