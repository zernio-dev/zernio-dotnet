# Zernio.Model.PostAuthenticity

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PostId** | **string** | The external post the score belongs to | 
**Score** | **int** | Higher means the view pattern looks more organic | 
**Confidence** | **decimal** | How much data the score rests on | 
**Reasons** | [**List&lt;PostAuthenticityReasonsInner&gt;**](PostAuthenticityReasonsInner.md) | Each factor that lowered the score, with its weight in points | 
**VarVersion** | **string** | Scoring model version | 
**ComputedAt** | **DateTime** |  | 
**SampleCount** | **int** | Number of samples the score was computed from | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

