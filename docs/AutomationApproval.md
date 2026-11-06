# Zernio.Model.AutomationApproval
A request an automation sent for a person's approval before acting, with each change it holds.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**AutomationId** | **string** |  | 
**CheckId** | **string** | The check that found the matches and sent the request. | 
**Status** | **string** | &#x60;cancelled&#x60; when the automation stopped asking for approval before anyone decided. | 
**To** | **List&lt;string&gt;** | The emails the request was sent to. | 
**ExpiresAt** | **DateTime** | After this the request can no longer be decided and its changes are skipped. | 
**CreatedAt** | **DateTime** |  | 
**DecidedBy** | [**AutomationApprovalDecidedBy**](AutomationApprovalDecidedBy.md) |  | 
**DecidedAt** | **DateTime?** |  | 
**CanDecide** | **bool** | True when the request is pending and you are one of the approvers the automation names now. | 
**Changes** | [**List&lt;AutomationApprovalChange&gt;**](AutomationApprovalChange.md) | The changes the request holds. Notifications are not listed. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

