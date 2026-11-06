# Zernio.Model.AutomationApprovalStep
Makes the ad rule wait for a person's OK before it acts. One per ad rule, placed before the change. Each change waits until one of `to` approves it, for `expiresIn` at most. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Type** | **string** |  | 
**To** | **List&lt;string&gt;** | Team members, by email. Each once. | 
**ExpiresIn** | **string** | From &#x60;15m&#x60; to &#x60;7d&#x60;, in whole minutes. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

