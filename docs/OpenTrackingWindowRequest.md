# Zernio.Model.OpenTrackingWindowRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PostId** | **string** | Id of an external post. Required unless &#x60;accountId&#x60; and &#x60;url&#x60; are both sent. | [optional] 
**AccountId** | **string** | Connected account the post belongs to. Send together with &#x60;url&#x60;. | [optional] 
**Url** | **string** | Public URL of the post on the platform. Send together with &#x60;accountId&#x60;. | [optional] 
**TrackingDays** | **int** | How many days the window stays open. | [optional] [default to 30]
**RequestedBy** | **string** | Free-form label for who asked for the window. It is stored and returned as given. | [optional] [default to "api"]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

