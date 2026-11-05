# Zernio.Model.DuplicateAdCampaign200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CopiedCampaignId** | **string** | Platform ID of the new campaign | [optional] 
**AdSetIdMap** | **Dictionary&lt;string, string&gt;** | Meta only: source ad set ID to copied ad set ID. Empty when &#x60;deepCopy&#x60; is false. | [optional] 
**AdIdMap** | **Dictionary&lt;string, string&gt;** | Meta only: source ad ID to copied ad ID, across every copied ad set. Empty when &#x60;deepCopy&#x60; is false. | [optional] 
**Discovery** | **string** | The copy exists on the platform in all three cases.  - &#x60;triggered&#x60;: an ads sync started and runs after this response, so the copy may not be readable through Zernio yet. - &#x60;skipped&#x60;: no sync started, so the copy appears on a later scheduled sync. - &#x60;failed&#x60;: the sync could not start. A sync that errors after the response is not reported here. | [optional] 
**Raw** | **Object** | Platform-native response from the copy (TikTok and LinkedIn). Absent on Meta, which returns &#x60;adSetIdMap&#x60; and &#x60;adIdMap&#x60; instead. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

