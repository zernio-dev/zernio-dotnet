# Zernio.Model.SelectGoogleBusinessLocation200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Message** | **string** |  | [optional] 
**RedirectUrl** | **string** | Redirect URL if custom redirect_url was provided | [optional] 
**Account** | [**SelectGoogleBusinessLocation200ResponseAccount**](SelectGoogleBusinessLocation200ResponseAccount.md) |  | [optional] 
**Accounts** | **List&lt;Object&gt;** | locations with two or more distinct entries only. The connected accounts, same shape as &#x60;account&#x60;. The redirect_url then carries &#x60;accountIds&#x60; (comma-separated) and &#x60;accountId&#x60; of the first. | [optional] 
**Failed** | [**List&lt;SelectGoogleBusinessLocation200ResponseFailedInner&gt;**](SelectGoogleBusinessLocation200ResponseFailedInner.md) | locations only. The locations that could not be connected while the others were. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

