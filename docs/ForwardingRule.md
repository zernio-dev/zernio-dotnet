# Zernio.Model.ForwardingRule

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Rule ID, used to delete it. | [optional] 
**ProfileId** | **string** |  | [optional] 
**AccountId** | **string** |  | [optional] 
**DestinationId** | **string** | Platform destination (pixel, conversion action, rule, ...). | [optional] 
**EventNames** | **List&lt;string&gt;** | Event names forwarded to this destination; null forwards every event. | [optional] 
**Sources** | **List&lt;ForwardingRule.SourcesEnum&gt;** | Event sources forwarded to this destination; null forwards events from every source. | [optional] 
**ApiSecretVerified** | **bool** | Only when an &#x60;apiSecret&#x60; was saved by this request. Google Analytics never confirms a Measurement Protocol API secret, so it is &#x60;false&#x60; there: the first events in GA4 Realtime prove the secret is right. | [optional] 
**EventNameMap** | **Dictionary&lt;string, string&gt;** | Renames events for this destination, such as &#x60;{ \&quot;Lead\&quot;: \&quot;Purchase\&quot; }&#x60;; null sends every event under its own name. | [optional] 
**ValueOverride** | [**ForwardingRuleValueOverride**](ForwardingRuleValueOverride.md) |  | [optional] 
**ValueCondition** | [**ForwardingRuleValueCondition**](ForwardingRuleValueCondition.md) |  | [optional] 
**EventValues** | [**Dictionary&lt;string, ForwardingRuleEventValue&gt;**](ForwardingRuleEventValue.md) | The value this destination gets for each event name, keyed by the name as received (before &#x60;eventNameMap&#x60; renames it), such as a &#x60;Lead&#x60; worth 20 EUR and a &#x60;QualifiedLead&#x60; worth 150 EUR. An event listed here ignores &#x60;valueOverride&#x60;; events not listed keep it.  The dashboard&#39;s Value sent section (Ads, Conversions, a destination) sets this map. | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

