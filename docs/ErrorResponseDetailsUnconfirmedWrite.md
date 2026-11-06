# Zernio.Model.ErrorResponseDetailsUnconfirmedWrite
Meta ad create failures only. Set when Meta answered a create with a 5xx or a non-JSON body, or dropped the connection after the request was sent, and reading the parent back by name did not settle it. Zernio did not retry it.  One of these left it open:  - The read-back found several objects of the same name. - The parent could not be read, or the object is a creative, which has no reliable read-back. - The read-back found no such object, after a dropped connection, a non-JSON body, a 5xx with `retryOnServerError: false`, or a 5xx on a create whose own body is `status: ACTIVE`. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** |  | [optional] 
**ParentId** | **string** | Where to look for it: the ad set for an ad, the campaign for an ad set, the ad account otherwise. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

