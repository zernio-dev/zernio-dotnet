# Zernio.Model.UpdateAdSetStatus200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Status** | **string** | The status written to the ad set. Absent when nothing was written (see message). | [optional] 
**Updated** | **int** | Number of ads whose own stored status changed too. 0 is normal on a resume whose ads are all awaiting the platform. | [optional] 
**Skipped** | **int** | Number of ads whose own status was left as it was | [optional] 
**SkippedReasons** | **List&lt;string&gt;** | Why each group of ads was skipped | [optional] 
**Message** | **string** | Present only where the platform has no ad-set switch and no child ad was actionable | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

