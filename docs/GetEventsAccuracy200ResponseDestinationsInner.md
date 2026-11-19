# Zernio.Model.GetEventsAccuracy200ResponseDestinationsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**RuleId** | **string** | The forwarding rule. | [optional] 
**ProfileId** | **string** |  | [optional] 
**AccountId** | **string** |  | [optional] 
**Platform** | **string** | Ad platform, such as &#x60;metaads&#x60; or &#x60;googleads&#x60;. | [optional] 
**AccountName** | **string** |  | [optional] 
**DestinationId** | **string** |  | [optional] 
**Sales** | **int** | Real sales in the period from the sources the rule takes. | [optional] 
**Sent** | **int** | Sales a send was tried for. | [optional] 
**Accepted** | **int** | Sales the platform accepted, by the latest attempt. | [optional] 
**Failed** | **int** |  | [optional] 
**Retrying** | **int** |  | [optional] 
**NotSent** | **int** | Sales never sent: no ad consent, no identifier the platform matches on, or left out by the rule&#39;s event names. | [optional] 
**Accuracy** | **decimal?** | &#x60;accepted / sent&#x60;, from 0 to 1. &#x60;null&#x60; with no sale sent. | [optional] 
**Deliveries** | [**GetEventsAccuracy200ResponseDestinationsInnerDeliveries**](GetEventsAccuracy200ResponseDestinationsInnerDeliveries.md) |  | [optional] 
**Match** | [**GetEventsAccuracy200ResponseDestinationsInnerMatch**](GetEventsAccuracy200ResponseDestinationsInnerMatch.md) |  | [optional] 
**MatchRate** | **decimal?** | &#x60;match.identified / match.events&#x60;. &#x60;null&#x60; with nothing sent. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

