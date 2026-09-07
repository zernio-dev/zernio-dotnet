# Zernio.Model.CreateConversionActionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | SocialAccount ID. Must be a &#x60;googleads&#x60; account. | 
**CustomerId** | **string** | Google Ads customer id (digits only). Resolved automatically when the connection has exactly one accessible customer. | [optional] 
**Name** | **string** |  | 
**Type** | **string** | Only WEBPAGE is supported for creation today. | 
**DefaultValue** | **decimal** | Default conversion value used when an event doesn&#39;t carry its own value. | [optional] 
**AlwaysUseDefaultValue** | **bool** | When true, always use defaultValue and ignore any value sent with the event. Defaults to true when defaultValue is set. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

