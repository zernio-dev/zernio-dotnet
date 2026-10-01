# Zernio.Model.SelectInstagramAccountRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** | Profile ID from your connection flow | 
**PageId** | **string** | The Facebook Page ID selected by the user, from GET /v1/connect/instagram/select-account. Send this or pageIds, not both. | [optional] 
**PageIds** | **List&lt;string&gt;** | Several Page IDs whose linked Instagram accounts to connect from one sign-in, each as its own account. With two or more distinct IDs the response lists &#x60;accounts&#x60; and &#x60;failed&#x60; instead of &#x60;account&#x60;, and the request is refused with 400 while a profile holds one Instagram account and on a reconnect or an ads connect. A single distinct ID behaves exactly like pageId. | [optional] 
**TempToken** | **string** | Long-lived Facebook user access token from the OAuth callback redirect | 
**RedirectUrl** | **string** | Optional custom redirect URL to return to after selection | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

