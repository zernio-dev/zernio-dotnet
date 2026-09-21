# Zernio.Model.CreateImessageOptInLinkRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Body** | **string** | Prefilled message text. Must contain the literal &#x60;[opt-in-code]&#x60; placeholder, e.g. \&quot;Hi! My code is [opt-in-code]\&quot;. | 
**Parameters** | **Dictionary&lt;string, string&gt;** | Custom key/values (e.g. leadId, campaign) echoed back on the opt-in message. | [optional] 
**OptInCode** | **string** | Your own code in place of the generated one (3-8 characters, no spaces or &#x60;#&#x60;, &#x60;!&#x60;, &#x60;-&#x60;). An unredeemed link lives 24 hours; re-issuing with the same code replaces it, and the earlier URL stops matching. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

