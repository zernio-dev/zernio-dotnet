# Zernio.Model.SupportRunDiagnosis

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Category** | **string** | What kind of problem the answer describes. New values may be added: treat any value you do not recognize as &#x60;other&#x60;. | 
**Cause** | **string** | The cause the answer gives, in one sentence. Null when the answer reports no problem, for example a how-to question. | 
**FixSteps** | **List&lt;string&gt;** | The steps the answer recommends, in order. Empty when it recommends none. | 
**DocsLinks** | **List&lt;string&gt;** | Links to docs.zernio.com that the answer itself cites. Empty when it cites none. | 
**WhoMustAct** | **string** | Who has to act to resolve it: you (&#x60;integrator&#x60;), your end user, Zernio, the social platform, or nobody. New values may be added: treat any value you do not recognize as &#x60;none&#x60;. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

