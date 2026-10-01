# Zernio.Model.SelectLinkedInOrganizationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** |  | 
**TempToken** | **string** |  | 
**UserProfile** | **Object** |  | 
**AccountType** | **string** | Send this (with selectedOrganization for an organization) or selections, not both. | [optional] 
**Selections** | [**List&lt;SelectLinkedInOrganizationRequestSelectionsInner&gt;**](SelectLinkedInOrganizationRequestSelectionsInner.md) | Several accounts to connect from one sign-in (yourself and/or organizations), each as its own account. With two or more entries the response lists &#x60;accounts&#x60; and &#x60;failed&#x60; instead of &#x60;account&#x60;, and the request is refused with 400 while a profile holds one LinkedIn account and on a reconnect or an ads connect. A single entry behaves exactly like accountType. | [optional] 
**SelectedOrganization** | [**SelectLinkedInOrganizationRequestSelectedOrganization**](SelectLinkedInOrganizationRequestSelectedOrganization.md) |  | [optional] 
**RedirectUrl** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

