# Zernio.Model.CreateCustomConversionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdAccountId** | **string** | Meta ad account id (act_&lt;n&gt;). | 
**Name** | **string** | Also the reuse key, together with pixelId. | 
**PixelId** | **string** | Meta pixel id (event_source_id). From GET /v1/accounts/{accountId}/tracking-tags. | 
**CustomEventType** | **string** | Meta custom_event_type, e.g. LEAD, PURCHASE, OTHER. | 
**Rule** | **Object** | Meta conversion rule, forwarded verbatim. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

