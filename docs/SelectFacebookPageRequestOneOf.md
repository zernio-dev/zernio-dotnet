# Zernio.Model.SelectFacebookPageRequestOneOf

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** | Profile ID from your classic connection flow. | 
**PageId** | **string** | The Facebook Page ID selected by the user. Send this or pageIds, not both. | [optional] 
**PageIds** | **List&lt;string&gt;** | Several Page IDs to connect from one sign-in, each as its own account. With two or more distinct IDs the response lists &#x60;accounts&#x60; and &#x60;failed&#x60; instead of &#x60;account&#x60;, and the request is refused with 400 on a reconnect or an ads connect, which pick exactly one Page. A single distinct ID behaves exactly like pageId. | [optional] 
**TempToken** | **string** | Temporary Facebook access token from OAuth. | 
**UserProfile** | [**SelectFacebookPageRequestOneOfUserProfile**](SelectFacebookPageRequestOneOfUserProfile.md) |  | 
**RedirectUrl** | **string** | Optional custom redirect URL to return to after selection. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

