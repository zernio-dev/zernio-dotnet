# Zernio.Model.GetVoiceCallEstimate200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Via** | **string** |  | [optional] 
**DestinationCountry** | **string** | ISO country of &#x60;to&#x60;. Isle of Man, Jersey and Guernsey numbers return IM, JE and GG. | [optional] 
**LineType** | **string** | Line type of &#x60;to&#x60;. Where it is not &#x60;mobile&#x60; or &#x60;landline&#x60;, &#x60;perMinuteUsd&#x60; takes the dearer of the two. | [optional] 
**CallerId** | **string** | Caller ID the rates were picked for. Voice API estimates without &#x60;from&#x60; use your first calling number. | [optional] 
**CallerCountry** | **string** |  | [optional] 
**Minutes** | **int** |  | [optional] 
**PerMinuteUsd** | **decimal** | Billable cost per minute for &#x60;to&#x60;&#39;s line type and the requested options. | [optional] 
**BillingIncrementSeconds** | [**GetVoiceCallEstimate200ResponseBillingIncrementSeconds**](GetVoiceCallEstimate200ResponseBillingIncrementSeconds.md) |  | [optional] 
**Rates** | [**GetVoiceCallEstimate200ResponseRates**](GetVoiceCallEstimate200ResponseRates.md) |  | [optional] 
**Trunk** | [**GetVoiceCallEstimate200ResponseTrunk**](GetVoiceCallEstimate200ResponseTrunk.md) |  | [optional] 
**Breakdown** | [**GetVoiceCallEstimate200ResponseBreakdown**](GetVoiceCallEstimate200ResponseBreakdown.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

