# Zernio.Model.UpdateAdAccountManagerLinkRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Stage** | **bool** | Send true to store this write as a staged change instead of applying it. The response is &#x60;202&#x60; with the change, and POST /v1/ads/changes/{changeId}/confirm applies it later. Cannot be combined with &#x60;validateOnly&#x60;. | [optional] 
**AccountId** | **string** | Google ads SocialAccount id. | 
**ManagerCustomerId** | **string** | Manager customer id, digits only. | 
**ClientCustomerId** | **string** | Client customer id, digits only. | 
**ManagerLinkId** | **string** | Numeric link id from GET /v1/ads/accounts/hierarchy. | 
**Action** | **string** |  | 
**ValidateOnly** | **bool** |  | [optional] [default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

