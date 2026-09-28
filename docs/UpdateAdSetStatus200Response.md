# Zernio.Model.UpdateAdSetStatus200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Status** | **string** | The status written to the ad set switch | [optional] 
**Updated** | **int** | Number of ads whose own stored status changed too. 0 is normal on a resume whose ads are all awaiting the platform. | [optional] 
**Skipped** | **int** | Number of ads whose own status was left as it was | [optional] 
**SkippedReasons** | **List&lt;string&gt;** | Why each group of ads was skipped (for example \&quot;2 ads already switched off\&quot;, read from each ad&#39;s own switch) | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

