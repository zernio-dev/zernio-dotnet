# Zernio.Model.GetAccountHealth200ResponsePlatformConnectionMessagingBlockersInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EntityType** | **string** | Meta entity the reason is on (for example PHONE_NUMBER, WABA, BUSINESS) | [optional] 
**CanSendMessage** | **string** | That entity&#39;s state (LIMITED or BLOCKED) | [optional] 
**Code** | **int?** | Meta error code. &#x60;null&#x60; for an &#x60;additional_info&#x60; line. | [optional] 
**Description** | **string** | Meta&#39;s error description, or the &#x60;additional_info&#x60; line as Meta wrote it | [optional] 
**PossibleSolution** | **string** | Meta&#39;s suggested fix, when it gives one | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

