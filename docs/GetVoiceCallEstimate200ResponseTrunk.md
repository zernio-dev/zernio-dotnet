# Zernio.Model.GetVoiceCallEstimate200ResponseTrunk
Trunk calls only. Whether the trunk's limits would refuse this call.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Trunk the limits were read from. Null when none was resolved and the defaults apply. | [optional] 
**LimitsSource** | **string** |  | [optional] 
**MaxDestinationRateUsd** | **decimal?** | Per-minute cap, compared with the carrier&#39;s rate for the route (half the billed rate). Default 0.30, null when the trunk has no cap. | [optional] 
**DestinationWhitelisted** | **bool** | Whether destinationCountry is on the trunk&#39;s whitelist. The default whitelist is every country Zernio sells numbers in. | [optional] 
**RateCheck** | **string** | &#x60;partial&#x60; means some of the destination&#39;s networks are above the cap and calls to them are refused. | [optional] 
**OutboundEnabled** | **bool?** | False while outbound is paused for an unfunded balance. Null with default limits. | [optional] 
**WouldBlock** | **bool** |  | [optional] 
**BlockReasons** | **List&lt;GetVoiceCallEstimate200ResponseTrunk.BlockReasonsEnum&gt;** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

