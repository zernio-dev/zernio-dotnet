# Zernio.Model.ErrorResponseDetailsUnconfirmedWrite
Meta ad create failures only, when Meta answered a create with a 5xx or a non-JSON body, or dropped the connection after the request was sent, and reading the parent back by name did not settle it: several objects of the same name, a parent that could not be read, or (after a dropped connection, a non-JSON body, or a 5xx with `retryOnServerError: false`) no such object. Zernio did not retry it.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** |  | [optional] 
**ParentId** | **string** | Where to look for it: the ad set for an ad, the campaign for an ad set, the ad account otherwise. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

