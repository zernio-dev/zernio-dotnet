# Zernio.Model.EstimateAdReach200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Available** | **bool** | Whether a pre-flight estimate is available on this platform. False for Google and TikTok. | 
**Lower** | **int** | Lower bound of the estimated reachable audience. Present only when available. | [optional] 
**Upper** | **int** | Upper bound of the estimated reachable audience. Present only when available. | [optional] 
**Daily** | **int** | Optional estimated daily reach/results at the given budget, when the platform returns it. | [optional] 
**Currency** | **string** | Currency of any monetary fields in the estimate, when applicable. | [optional] 
**EstimateReady** | **bool** | Meta only. False when Meta is still computing the estimate (the audience is too new); retry shortly. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

