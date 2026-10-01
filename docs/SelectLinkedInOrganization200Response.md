# Zernio.Model.SelectLinkedInOrganization200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Message** | **string** |  | [optional] 
**RedirectUrl** | **string** | The redirect URL with connection params appended (only if redirect_url was provided in request) | [optional] 
**Account** | [**SelectLinkedInOrganization200ResponseAccount**](SelectLinkedInOrganization200ResponseAccount.md) |  | [optional] 
**Accounts** | **List&lt;Object&gt;** | selections only. The connected accounts, same shape as &#x60;account&#x60;. The redirect_url then carries &#x60;accountIds&#x60; (comma-separated) and &#x60;accountId&#x60; of the first. | [optional] 
**Failed** | [**List&lt;SelectLinkedInOrganization200ResponseFailedInner&gt;**](SelectLinkedInOrganization200ResponseFailedInner.md) | selections only. The accounts that could not be connected while the others were. &#x60;id&#x60; is the organization URN or the member id, or &#x60;selections[i]&#x60; for an entry naming neither. | [optional] 
**BulkRefresh** | [**SelectLinkedInOrganization200ResponseBulkRefresh**](SelectLinkedInOrganization200ResponseBulkRefresh.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

