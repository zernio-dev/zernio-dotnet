# Zernio.Model.CreateCrmActivityRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Body** | **string** | The text to log. | 
**Subject** | **string** | Salesforce Task subject (default &#x60;&lt;Channel&gt; activity (&lt;direction&gt;)&#x60;); on HubSpot, the bold first line. | [optional] 
**Channel** | **string** |  | [optional] [default to ChannelEnum.Other]
**Direction** | **string** |  | [optional] 
**OccurredAt** | **DateTime** | When it happened. Defaults to now. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

