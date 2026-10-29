# Zernio.Model.DuplicateAdSet200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CopiedAdSetId** | **string** | Platform ID of the new ad set | [optional] 
**CopiedAdIds** | **List&lt;string&gt;** | Platform IDs of the copied ads | [optional] 
**AdIdMap** | **Dictionary&lt;string, string&gt;** | Meta only: source ad ID to copied ad ID. Empty when &#x60;deepCopy&#x60; is false. | [optional] 
**Discovery** | **string** |  | [optional] 
**Raw** | **Object** | Platform-native response from the copy (TikTok). Absent on Meta, which returns &#x60;adIdMap&#x60; instead. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

