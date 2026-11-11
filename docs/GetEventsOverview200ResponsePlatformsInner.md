# Zernio.Model.GetEventsOverview200ResponsePlatformsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | [optional] 
**Platform** | **string** | Ad platform, such as &#x60;metaads&#x60; or &#x60;googleads&#x60;. | [optional] 
**AccountName** | **string** |  | [optional] 
**DestinationName** | **string** | The destination (pixel, dataset or conversion action) id. | [optional] 
**SentToday** | **int** | Events the platform accepted today. | [optional] 
**FailedToday** | **int** | Events that failed for good today. | [optional] 
**LastSentAt** | **DateTime?** | Last accepted send in the last 30 days. | [optional] 
**LastEventName** | **string** | Name of the event in that send. | [optional] 
**LastError** | **string** | The platform&#39;s error on the last failed send in the last 30 days. | [optional] 
**FixUrl** | **string** | Where to fix a failing destination. Always &#x60;null&#x60; for now. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

