# Zernio.Model.CreateTrackingTagEventRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdAccountId** | **string** | Scopes the lookup on platforms whose tag ids live inside an ad account. | [optional] 
**Name** | **string** |  | 
**Type** | **string** | The platform&#39;s own event type enum value (e.g. &#x60;PURCHASE&#x60;). | [optional] 
**SiteEvent** | **string** | Neutral alternative to &#x60;type&#x60;, mapped to the platform&#39;s closest type. | [optional] 
**Enabled** | **bool** |  | [optional] 
**DefaultValue** | **decimal** |  | [optional] 
**Currency** | **string** | ISO 4217 code. | [optional] 
**ClickWindowDays** | **int** |  | [optional] 
**ViewWindowDays** | **int** |  | [optional] 
**UrlContains** | **string** | Fire only on pages whose URL contains this text (case-insensitive). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

