# Zernio.Model.CreateOAuthAppRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** | One of the platforms listed in &#x60;platforms&#x60; of GET /v1/connect/oauth-apps. | 
**Label** | **string** |  | 
**ClientId** | **string** |  | 
**ClientSecret** | **string** |  | 
**ScopeAreas** | **List&lt;CreateOAuthAppRequest.ScopeAreasEnum&gt;** | Areas this app requests. Defaults to every area the platform supports; an area the platform cannot request separately is a 400. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

