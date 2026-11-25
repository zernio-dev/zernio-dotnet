# Zernio.Model.StagedAdChangeError
Present once `failed`, and on a staged change marked `stale`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **string** | An error code, or &#x60;target_changed&#x60; when the object changed on the ad network after staging. | [optional] 
**Message** | **string** |  | [optional] 
**Details** | **Dictionary&lt;string, Object&gt;** | Creates only. What the failed create reported, such as objects it had already made on the ad network. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

