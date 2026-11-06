# Zernio.Model.AutomationApprovalChange

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ActionId** | **string** |  | 
**Subject** | [**AutomationApprovalChangeSubject**](AutomationApprovalChangeSubject.md) |  | 
**Type** | **string** |  | 
**Previous** | [**AutomationApprovalChangePrevious**](AutomationApprovalChangePrevious.md) |  | 
**Target** | [**AutomationApprovalChangeTarget**](AutomationApprovalChangeTarget.md) |  | 
**Conditions** | **List&lt;Object&gt;** | Each condition as it was judged when the request was sent, with its actual value. | 
**Status** | **string** | &#x60;pending&#x60; until the request is decided. | 
**Reason** | **string** | Why the change was made, skipped or failed, when known. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

